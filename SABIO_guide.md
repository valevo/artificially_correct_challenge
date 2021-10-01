# SABIO


## Introduction




## Data Format & Preparation

The data format on which SABIO works is fairly simple: a table of objects with, aside from basic
information, two types of properties. First, there are fields for filtering and organising
objects, such as dates or classifications and second, textual fields for searching objects
based on terms and for scoring by our bias scoring algorithms. To keep things maximally general,
SABIO admits arbitrary fields of both types whose semantics are specified along with the data.

Basic properties of objects are an ID, which is used to refer to object within SABIO, a title 
(or name) and a date (those can admittedly be a bit complicated). All other fields are generally
optional but then of course, filtering, searching and scoring objects doesn't make much sense. 





#### The NMvW Data in CSV

Here is an excerpt from the data of the Dutch Museum of World Cultures (NMvW), transformed by into a CSV format that SABIO can work with. 

Notice that the NMvW data hasv two dates (`BeginISODate` & `EndISODate`) instead of just one; this is because for most objects, there is uncertainty about the actual date the object was created. `Dated` is a non-parseable string that gives more details about the date of an object.



 - the main table:

    | ObjectID | Title | Description | BeginISODate | EndISODate | Dated | Department | Classification | Medium |
    |----------|-------|-------------|--------------|------------|-------|------------|---------------|--------| 
    |  1       | "BESCHILDERDE EN GEVLOCH..."| ""   | 0   | 2011 | voor 2011 | Insulair Zuidoost-Azie | Materiele cultuurcollectie | Wood |



 - meta table, indicating type and semantics of each field in the main table:

    | Field | Type | IsStringSearchField | IsSearchParameter | IsXValue | IsScoringField |
    |-------|------|---------------------|-------------------|----------|----------------|
    |  ObjectID | int  | 0                   | 0                 | 0        | 0 |             
    |     Title | str  | 1                   | 0                 | 0        | 1 |
    |  Descripti| str  | 1                   | 0                 | 0        | 1 |
    | BeginISOD| date | 0                   | 1                 | 1        | 0 |
    |   EndISOD| date | 0                   | 1                 | 1        | 0 |
    |   Dated  | str  | 0                   | 0                 | 0        | 0 |
    | Departmen| str  | 0                   | 1                 | 1        | 0 |
    | Classific| str  | 0                   | 1                 | 1        | 0 |
    
   The meta table indicates that `Title` and `Description` are both used to search for objects and to score them with the bias scoring engines. `BeginISODate`, `EndISODate`, `Department` and `Classification` are both parameters for filtering objects (`IsSearchParameter`) and for organising them on the x-axis of the graphical interface.
      
      
      
#### General CSV Data Specification


 - main CSV:


 | ID | Title | Description | Date | TextField1 | ... | TextField_k | ParamField1 | ... | ParamField_n |
 |----|-------|-------------|------|------------|-----|-------------|-------------|-----|--------------|
 | 01 | "The Potato Eaters" | "Painting of peasants eating potatoes." | 13-04-1885 | "V. van Gogh" | ... | "Painted in Nuenen" | "Painting" | ... | "Western Art" |
 | 02 | "Still Life of Fish and Cat" | "Depicts fish and a cat." | 1620 | "Clara Peeters" | ... | "" | "Painting" | ... | "Western Art" |


 - corresponding meta table:


  | Field | Type | IsStringSearchField | IsSearchParameter | IsXValue | IsScoringField |
  |-------|------|---------------------|-------------------|----------|----------------|
  | ID    |  any | 0 | 0 | 0 | 0|
  | Title | str  | 1 | 0 | 0 | 1|
  | Description | str | 1 | 0 | 0 | 1 |
  | Date | date | 0 | 1 | 1 | 0 |
  | TextField1 | str | 1 | 0 | 0 | 0 |
  | TextField2 | str | 1 | 0 | 0 | 1 |  
  | TextField2 | str | 0 | 0 | 0 | 1 |
  | ParamField1 | str | 0 | 1 | 0 | 0 |
  | ParamField2 | str | 0 | 0 | 1 | 0 |
  | ParamField3 | str | 0 | 1 | 1 | 0 |

