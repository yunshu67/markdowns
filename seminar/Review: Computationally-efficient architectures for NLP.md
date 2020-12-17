#### Review: Computationally-efficient architectures for NLP

# Major contributions of the article

This article mainly contributes to discussing the computationally-efficient architectures for *natural language processing* (short: NLP) . More specifically, it covers some of the most efficient architectures for NLP: 

- the basic concepts needed for these architectures
- the principle of these architectures
- efficiency analysis and possible improvements



# Quality of the manuscript

  The quality of this article is good overall. By introducing a technology about word representation (*word2vec*), the author lead us to the most basic problem that people will encounter in NLP: word embedding, i.e, using vectors to represent words. Then, the author introduced us to two commonly used models for word2vec: *CBOW* and *Skip-Gram*, as well as the basic technologies used in these models: *softmax function* (CBOW) and *hierarchical softmax function* (Skip-Gram). By comparing these two functions , the author showed us why Skip-Gram is more computationally-efficient than CBOW.  After that, the author introduced other techniques in NLP such as seq2seq and transformer, including their architectures, their core ideas, and their efficiency analysis (not finished yet).

  This article has a clear line of thought and a clear structure, is closely related to the topic and has a strong coherence among the most sections. The author is good at using simple examples and figures, so that these architectures are very easy to understand, which I think is very good.

  However, this article still have improvement space.

# General remarks/corrections

1. About format:

   - typos:

     in the 7th line in the 1st section:

     > ... and the influence these architectures ~~had~~ `have` for further development ...

     near the 11th line in the subsection D, section 2:

     >  ~~I~~ `In` our case, ...

   - context mismatch

     At the very beginning of subsection B, section 2, the model **CBOW** is introduced. However, in the following part of this subsection it's all **COBOW**.

     I'm not sure whether it's a typo issue, but I would like to point it out here, I mean, if it's not a typo issue, the author should also explain the difference between CBOW and COBOW.

     By the way, it's also better if CBOW/COBOW could be shortly explained what they exactly stand for.

   - grammar mistakes:

     in the 3rd line, subsection C, section 2:

     > , ~~which~~ `whose` purpose is to...

     near the 12th line, subsection D, section 2:

     > root to node w, ~~which~~ `whose` probability is calculated ...

     In the third-to-last line, subsection D, section 2:

     > which results 1 in case ~~of~~ `where`/`that` x is true ...

2. About content:

   - no comparison between **word2vec** and **seq2seq**.

     Obviously these are two completely different techniques, but there is no comparison between them.

     I'm not sure whether seq2seq is an upgraded version of word2vec, but I would suggest the author to make a simple comparison of these two (in terms of computational efficiency)

   - figure 6 could be described more detailed

     As I said, almost all the figures are very clearly described. However, figure 6 is not. And furthermore figure 6 is very complicated, so I think it deserves a better explanation.

   - need more focus on why these architectures are efficient
     
     The article introduce the features, the structures, the core ideas and so on of the architectures, however,  since the topic is about **computationally efficient**, the author should have more focus on why they are computationally efficient, instead of only introducing how the architectures work.
     
     Here personally I would suggest the author to open one subsection specifically to analysis the computational efficiency for each architecture, rather than in pieces.