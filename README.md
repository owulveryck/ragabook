# ragabook
A set of Go tools to query books with OpenAI's API and the RAG system

Source of inspiration (and of code): [Retrieval Augmented Generation in Go](https://eli.thegreenplace.net/2023/retrieval-augmented-generation-in-go/)

# Story...
I wanted to play with the concept of [RAG](https://fr.wikipedia.org/wiki/Ing%C3%A9nierie_de_prompt#G%C3%A9n%C3%A9ration_augment%C3%A9e_par_r%C3%A9cup%C3%A9ration). My goal is to gradually approach an implementation "from scratch" to clarify the uncertainties I have in understanding the system.

**Note:** The "from scratch" approach is difficult because the generation of the embedding is linked to the model and tokenization, but let's consider it as "from scratch" in the Engineering part, which will be enough for me.
I used the information from [this article](https://eli.thegreenplace.net/2023/retrieval-augmented-generation-in-go/) because it's about Go, and I speak the language fluently.

What I needed was a use case.

## My use case
I often read books that I consider as "reference" (team topologies, DDD, ...). One of my current references is "[_the value flywheel effect_](https://itrevolution.com/product/the-value-flywheel-effect/)".

This book talks about strategy but also gives keys on how to use Simon Wardley's theory. They explain how to use maps with a CEO, or how to map a technological solution.

In the context of consulting missions, mapping is a valuable tool, and this book contains important information to make the best use of these tools.

For example, I have synthesized a [list of questions](https://gist.github.com/owulveryck/764b0e92850c157602b5abf8a4548ab5) that can serve as an interview framework in a consulting mission.

What I would like now is to "chat" with my virtual assistant to ask him specific questions and have him give me the answer using the book.

You have it: a RAG

## First step: POC and data

The first step in setting up a RAG is to retrieve the data and clean it up.
Indeed, you need to have the raw text somewhat enhanced. Markdown works very well in this case.

On the other hand, there is another "hiccup": you need the rights to do it... the book is not in the public domain. I will deal with that later. For now, to validate feasibility, I will use another book.
This book is in creative commons and already formatted. I know it and it is related to the subject: it is Simon Wardley's book.

**First lesson**: Owning the data is a strength... I've always been told that, but this is obvious.

### Data Retrieval

Simon Wardley's book has been converted into various formats. This [repository](https://github.com/andrewharmellaw/wardley-maps-book) provides a version in asciidoc. I want it in markdown, because I know that GPT-x is proficient in that language. A quick "`asciidoc` and `pandoc`" and there you go: a few markdown files of content.

**Second learning**: I was lucky because someone had already done the conversion work into a "digitally exploitable" format. This step can be lengthy. It's a job for a data engineer.

I then run the code for the website and now I have a `sqllite` database filled with chunks of Simon Wardley's book. It is within one of these chunks that my final program will search for the answer. Hopefully the text is cleanly divided and I don't end up with a chunk composed of the end of one chapter and the beginning of another. I would lose information.

**Third learning**: I used the default segmentation, but as PPR had told us, it would be wise to understand the data in order to organize it better. Nothing is magical. I know I will have a focus on this part.
## Second step: creating the embedding

This is a part that falls under engineering. This part will aim to convert pieces of text into a numerical representation (an array of numbers). This is what is called _embedding (or [word embedding](https://en.wikipedia.org/wiki/Word_embedding))._

As seen previously, the algorithm for converting words into vectors is linked to the model that we are going to use. Simply put, the program will call an API from OpenAI for each piece that will return the corresponding vector. This vector is then stored in the database.

**Interesting result**: I end up with a SQLLite database that contains Wardley's work with a mathematical representation usable with OpenAI.
## Last step: inference
Inference is the heart of my application: I ask a question, the application searches in my database for the piece that corresponds to the context, then sends everything to OpenAI which generates a response.

Here, no vector base, the search is simple:

- we calculate the embedding of the question (an API call in the same way as for calculating the embedding of the pieces)
- we perform a [similarity calculation](https://fr.wikipedia.org/wiki/Similarit%C3%A9_cosinus) with respect to each element in the base
- we take the best result, that is, the one that is most related to the question.
- we send it in _prompt_ mode to the LLM engine via API with the following question:

```
Use the below information to answer the subsequent question.
Information:
%v

Question: %v
```
**Fourth learning**: We enter into prompt engineering, I can replace my hard-coded question with something like:
```
Use the below information to answer the subsequent question and add the origin.
Origin: 

chapter %v

Information:
%v

Question: %v
```
To do this, I must then complete my initial database by adding, for each piece, its source. This requires a little thought about its use case in advance. In the exploratory space in POC mode, it's not a big deal, but when we want to "productize" the application, it will be annoying to change the database.

### Side note about the vector base

The similarity calculation is done manually in a large loop using a simple similarity calculation algorithm. If the number of pieces becomes too large (for example, if I want to index an entire library), this method will become inefficient. We will then switch to a vector base.
It is this last one that will find the best "neighbor". It remains to be seen which algorithms they use. Do all vector bases return the same result? This is an interesting point on which I think I need to form an opinion as a consultantResults, findings, and fun part

By compiling the program, I can query my knowledge base:

```
❯ ./rag -db=../../data/db/wardley.db -answer "give me examples of inertia" 2>/dev/null
1. Resistance to change in business due to past success and uncertainty in co-evolving practices.
2. Consumer concerns about disruption to past norms, transition to the new, and the agency of the new when adopting cloud computing.
3. Suppliers' inertia to change due to past financial success, internal resistance, and external market expectations.
4. Financial markets' inertia towards stability and past results.
5. Cultural inertia caused by past success in fulfilling a business model.
6. Resistance to change caused by cutting costs in response to declining revenue in a changing industry.
7. Inertia in reacting to disruptive changes in the market, such as the shift from products to utility services in computing.
8. Inertia in transitioning from custom-built solutions to product offerings.
9. Resistance to change in response to disruptive changes in various industries, leading to companies' demise.
10. Failure to adapt to predictable disruptions, such as the shift from products to utility services, leading to companies' downfall.
```
As the engine is the GPT-x language, I can even ask it in French, it will manage:

```
❯ ./rag -db=../../data/db/wardley.db -answer "donne moi tous les exemples d'inertie" 2>/dev/null
Les exemples d'inertie mentionnés dans le texte sont :
- "Perte de capital social" : résistance au changement due à des relations commerciales existantes avec des fournisseurs.
- "Peur, incertitude et doute" : tentative des fournisseurs de convaincre les équipes internes de ne pas adopter les nouveaux changements.
- "Perte de capital politique" : résistance au changement due à un manque de confiance envers la direction.
- "Barrières à l'entrée" : peur que le changement permette l'entrée de nouveaux concurrents.
- "Coût de l'acquisition de nouvelles compétences" : coût croissant de l'acquisition de nouvelles compétences en raison d'une demande accrue.
- "Adaptabilité" : préoccupations quant à la préparation du marché ou des clients au changement.
```
**Fifth learning**: here we can see that the results are less comprehensive. It is a help, but not a search engine. Idempotence stops at the moment of retrieving information from the embedding base. Then it's YOLO :D

## Conclusion and opening
The fun thing is that I end up with two self-contained assets:

- the binary in Go, which does not require installation. It is capable of querying any knowledge base in the format it was designed with
- the knowledge base `wardley.db`

Tomorrow, I can work on another book, generate the embedding, and share it. The better I divide it into pieces, the more useful the base will be... regardless of the inference engine.

**Last learning**: The versioning of the program is ultimately loosely coupled with my data. I can now clean and feed data independently of IT engineering... I should even be able to automate it through a pipeline.

So, if I send you the binary and the db file, you can query the knowledge base like me.

I will continue to play with this. I think I will add a small template engine for the question. The "chat" part will remain (for now it's just one question), but with OpenAI's APIs (or others), it's trivial.
