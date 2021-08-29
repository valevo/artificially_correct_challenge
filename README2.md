## `Artificially Correct` Challenge:
### Does Bias in Collections and Archives Survive Translation and Multilingualism?
The _Cultural AI Lab's_ Repo for the _Goethe Institute's_ _Artificially Correct_ Hackathon.


<img src="https://github.com/valevo/artificially_correct_challenge/blob/main/logo_white.jpg" alt="CulturalAI Logo" width="200"/>
https://www.cultural-ai.nl



1. **Background**: 

   In the [Cultural AI lab](https://www.cultural-ai.nl/) and in collaboration with the [National Museum of World Cultures](https://collectie.wereldculturen.nl/) (NMvW), we have been developing SABIO (the _SociAl BIas Observatory_): a tool and visual interface for exploratory analysis of bias and patterns of bias in museum collections and heritage archives. SABIO emphasises that researching bias is a social act and therefore, instead of automatically detecting [and judging] potential instances of bias, it is designed to provide access to paths through cultural datasets that lead users to discover bias in ways they might not [be able to] anticipate. To this end, SABIO consists of an extensible suite of parameterised algorithms that measure variables likely to _correlate_ with bias and (re-)orginasises the given collection according to these measurements and provides details about the origin individual values.
   
2. **Description**:

  So far, SABIO has been developed and tested exclusively on the NMvW's collection, a monolingual Dutch archive of around 800k objects with descriptions, titles and other meta-properties. At the same time, all of the design choices for SABIO have been made with the aim of maximal language independence and we would like to put this to the test. We therefore invite participants to experiment with and extend SABIO, or at least the algorithms it uses, in cross- and multilingual contexts. Potential tasks include but are by no means limited to:
  1. findinging and analysing an originally multilingual collection in SABIO and identifying patterns of bias across the languages present and how they translate
  2. similarly, machine translating a monolingual translation and analysing with the of SABIO how biases are transmitted and whether they survive automatic translation
  3. conceptual research on how paths in search of bias might be different across the languages present in a collection, and implementations based upon conclusions
  4. designing extensions to SABIO itself or to its algorithms that are tailored to comparison and highlighting of bias across languages
   

3. **Considerations**:

  1. Machine learning algorithms and their underlying datasets, such as the ones used by SABIO, require considerable computational resources and time; especially experimentation with such algorithms on large collections can be hindered by lack of resources 
  2. As of now, SABIO's data format is rather specific to the NMvW collection and thus requires specific properties to be present. We are working in the meantime on more general data specifications in order to fit other collections but this will likely restrict the choice of collection for the hackathon.
  3. Collections are often subject to copyright restrictions, which might not make it impossible to gain access but difficult and time-consuming.
  4. SABIO itself is a server-based application; even though it is entirely open-source, actually extending it or creating parallel versions requires server-side programming and resources for hosting.

4. **Resources**:

   - the SABIO interface to the NMvW collection (which is freely accessible)
   - SABIO's backend, written in Python, is available on our GitHub:  
     (1) data preprocessing scripts (to prepare a new dataset for input to SABIO)
     (2) search interface to the given collection
     (3) scoring algorithms to reorganise the dataset in terms of bias

6. **Skills**:

   Participants should have experience with either:
 
     - basic statistics and machine learning, specifically with natural language applications & (Python) programming
       (think of constructing word embeddings or defining and computing semantic association scores)
     - databases and digital archives (i.e. tabular data, RDF, etc), their intricacies and how to (pre-)process them for ML
       (e.g. building a database cleaning pipeline, basic natural language preprocessing on large sets of text)
     - doing research (historical, sociological, etc) on heritage collections, archives and the like
     - philosophical or sociological research on bias, especially in cultural contexts
  
   Optimally, the team would be made up of a mix of expertises in researching bias in cultural collections on the one hand and language processing on the other. 
   To be able to assess the quality and extent of the biases found with SABIO, it is useful if participants understand the language(s) of the input collection and therefore a team of speakers of different languages would be an advantage. 
   
   
7. Materials

     - screenshots of SABIO in action
     - screenshots of the NMvW data? search interface? tables?
 
 
