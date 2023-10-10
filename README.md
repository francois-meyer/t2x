# T2X

Triples-to-isiXhosa (T2X) is a data-to-text dataset for isiXhosa. It was constructed by translating part of the English [WebNLG dataset](https://synalp.gitlabpages.inria.fr/webnlg-challenge/challenge_2020/) and consists of triples of (subject, relation, object) mapped to descriptive sentences. It can be used to train sequence-to-sequence models for generating isiXhosa descriptions of structured triple data.

| Example #1              |  |
| :---------------- | :------: | 
| **Data triple**  | (South Africa, leaderName, Cyril Ramaphosa)       | 
| **English WebNLG** | Cyril Ramaphosa is the leader of South            |   
| **T2X isiXhosa translation** | uCyril Ramaphosa yinkokheli yoMzantsi Afrika    |  

| Example #2              |  |
| :---------------- | :------: | 
| **Data triple**  | (France, currency, Euro)       | 
| **English WebNLG** | The currency of France is the Euro            |   
| **T2X isiXhosa translation** | Imali yaseFransi yi-Euro    |  



### Dataset Details

| | Train              | Valid  | Test  |
| :---------------- | :------: | :------: | :------: | 
| English WebNLG 1-triples | 3,114 | 392 | 388 |
| T2X triples | 2,413 | 391 | 378 |
| T2X verbalisations | 3,859 | 600 | 888 |

The data covers 15 DBPedia categories. Three categories (Astronaut, Athlete and WrittenWork) are not included in the training data, only in the validation and test sets. In the training and validation sets, only one isiXhosa verbalisation per triple is given for a majority of the 371 domains, while the test set has multiple verbalisations (up to 3) for most examples, corresponding to multiple possible phrasings. 

### Data Annotation Process

Annotators, first language isiXhosa speakers who have studied the language at university level, were presented with the triples and English WebNLG verbalisations and asked to provide one or more isiXhosa translations which reflect the content of the triples while phrasing the translations as natural as possible. The verbalisations are relatively short, so translating them is an easy task given the isiXhosa proficiency of our annotators. Annotators discussed questions that arose during the translation process with each other, ensuring consistency among annotations.
