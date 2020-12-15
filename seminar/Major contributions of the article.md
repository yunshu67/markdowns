#### Review: Computational Aspects of Object Identification in Vision

# Major contributions of the article

  This article mainly contributes to discussing the computational aspects of object identification in vision. More specifically, it covers the computational challenges (section 2-4), algorithms and frameworks for object identification (section 5-7) and possible optimization approaches (section 8-9).



# Quality of the manuscript

  The quality of this article is good overall. Starting from the two common computational difficulties (*accuracy,* *efficiency* and their *trade-off*) of object identification algorithms, this article introduces the commonly used algorithm in object identification: *convolutional neural networks* (short: CNN) and two different frameworks based on CNN:  *region based (two stage) framework* and *unified (one stage) framework*, and discusses the performance of these two frameworks respectively around accuracy and efficiency. Furthermore, this article introduces several possible optimization approaches against accuracy and efficiency in terms of *object scale variations*, *intraclass variations* and *context*. 

  This article has a clear line of thought and a clear structure, is closely related to the topic and has a strong coherence among the most sections.

  However, the article still has improvement space.



# General remarks/corrections

1. About format:

   - blank lines between paragraphs should be unnecessary.

     Personally I don't think it's necessary to add blank lines between the paragraphs.

   - Some indents are missing in some paragraphs.

     I have noticed that in the most sections the first paragraph has an indent whereas the following paragraphs don't. I'm not sure whether it's ok to format like this, since the papers I've read have added indents to every single paragraph. Like I said before, there is an exception, i.e. the subsection B of section 7, where the first two paragraphs both have indents :)

   - Some clauses are missing comma, making it more difficult to read

     One example is in the 2nd paragraph, subsection A, section 5: 

     > While lower layers can detect patterns as edges and corners`,` higher layers can ...

   - duplicated phrase "with an stride of s"

     In line 4, subsection B, section 5:
     
     > the activation map, ~~with an stride of s~~. So ...
     
   - missing preposition
   
     In line 4, subsection B, section 5:
   
     > So n x n pooling scales down the original image to 1/n^2 `of` its original size ...
   
   - typos
   
     in last line of page 4:
   
     > ... of these models is still ~~to~~ `too` high for many usages, ...
   
   - *two* instead of *2*:
   
     One good writing habit is to write number in form of words instead of symbols.
   
     - examples: first line in 2nd paragraph, subsection A, section 8
   
2. About content
   
   - section 4 seems "independent" of other sections and less relative to *computational aspects*.
   
     Section 4 introduces several datasets used for object identification, which are almost not ever mentioned in the following parts of the article, and it only describes the features of different datasets, which don't have a direct connection to computational aspects of object identification.
   
     Here I would suggest the author should move one step further to computation aspects after describing the features of datasets, and echo this part in the conclusion section.
   
   - Figures are not described.
   
     I have noticed that all the figures don't have a description. This sometimes lead to a understanding problem, for instance figure 1 is very complicated and personally I don't understand it very well.
   
   - Section 5 (convolutional neural networks) could be more detailed.
   
     Since the fundamental algorithm used here is CNN, personally I think the author should explain it more in detail, since many technical terms are not explained, like "filter", "kernel", "activation maps", "receptive field"... 
   
     Because I'm only a bachelor student, I'm not very familiar with these terms, so I think it would be better if they are explained a little bit.
   
   - References can be added in some places.
   
     example: last line in page 4
   
     > especially on mobile devices `[*]`.
   
   
   
   
   
     
   
   