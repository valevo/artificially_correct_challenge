# artificially_correct_challenge
The _Cultural AI Lab's_ Repo for the _Goethe Institute's_ _Artificially Correct_ Hackathon


## CulturalAI  


<img src="https://github.com/valevo/artificially_correct_challenge/blob/main/logo_white.jpg" alt="CulturalAI Logo" width="200"/>




## SABIO Challenge

### Does Bias in Collections and Archives Survive Translation and Multilingualism?

In the [Cultural AI Lab](https://www.cultural-ai.nl/) and together with the [National Museum of World Cultures](https://collectie.wereldculturen.nl/), we are developing SABIO (The SociAl BIas Observatory), a tool for exploratory analysis of biases in museum collections and archives. With the help of a suite of machine learning algorithms that work on the textual entries present in a given collection, SABIO allows heritage professionals to 





1. **Background**: SABIO is a tool for exploration of bias in collections; it's an extensible suite of algorithms that reorganise collections and thus help navigating them visually; SABIO is meant to be an evolving tool that facilitates discovery of patterns of bias on the hand and that is perpetually updated on the other, resulting in a feedback loop of user and developer 

   - SABIO emphasises the aspect of bisa as a social and cultural act; its goal is to merely provide new, unseen paths towards 


2. **Description**:

   - so far, SABIO has only been developed and tested (not deployed yet) on the NMvW's collection which is monolingual Dutch; at the same time, all of SABIO's algorithms and interface have been built with the aim to be language independent as much as posssible (i.e. not relying, for instance, on hand-crafted language-specific corpora); a part of this challenge could be to test this by using SABIO on multilingual collections
 
   - this challenge consists of experimenting with SABIO (or at least the algorithms it consists of) in multilingual settings and extending SABIO with algorithms tailored for capturing bias in context of multi- or cross-lingual collections; potential tasks include: 
     - analysing an originally multilingual collection in SABIO and identifying patterns of bias across the languages present in the collection
     - designing extensions to SABIO, new algorithms or new dataset organisation levels, that are tailored for multilingual settings and that can facilitate comparison of bias across languages 
     - machine translating an originally monolingual collection, inputting it into SABIO and analysing whether and how bias survives 


3. **Considerations**:
   - machine learning algorithms (& underlying large data sets) can require considerable computation power  
     -> the DHLab can potentially provide some resources
   - actually extending SABIO requires rather heavy server-side (Python) programming   
     -> this can be done by us, so that the team members can focus on the content
   - SABIO is (currently) tailored towards the NMvW collection, requiring a rather specific format   
     -> we are working in the meantime on extending this format to fit other collections -> at the same time, this will restrict the choice of collections 
   - many collections are subject to copyright restriction, which may pose a hurdle in this challenge

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
 
 
