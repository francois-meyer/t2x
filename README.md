# T2X

Paper: [Triples-to-isiXhosa (T2X): Addressing the Challenges of Low-Resource Agglutinative Data-to-Text Generation](https://aclanthology.org/2024.lrec-main.1464.pdf)

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

### Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{meyer-buys-2024-triples,
    title = "Triples-to-isi{X}hosa ({T}2{X}): Addressing the Challenges of Low-Resource Agglutinative Data-to-Text Generation",
    author = "Meyer, Francois  and
      Buys, Jan",
    editor = "Calzolari, Nicoletta  and
      Kan, Min-Yen  and
      Hoste, Veronique  and
      Lenci, Alessandro  and
      Sakti, Sakriani  and
      Xue, Nianwen",
    booktitle = "Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024)",
    month = may,
    year = "2024",
    address = "Torino, Italia",
    publisher = "ELRA and ICCL",
    url = "https://aclanthology.org/2024.lrec-main.1464/",
    pages = "16841--16854",
    abstract = "Most data-to-text datasets are for English, so the difficulties of modelling data-to-text for low-resource languages are largely unexplored. In this paper we tackle data-to-text for isiXhosa, which is low-resource and agglutinative. We introduce Triples-to-isiXhosa (T2X), a new dataset based on a subset of WebNLG, which presents a new linguistic context that shifts modelling demands to subword-driven techniques. We also develop an evaluation framework for T2X that measures how accurately generated text describes the data. This enables future users of T2X to go beyond surface-level metrics in evaluation. On the modelling side we explore two classes of methods - dedicated data-to-text models trained from scratch and pretrained language models (PLMs). We propose a new dedicated architecture aimed at agglutinative data-to-text, the Subword Segmental Pointer Generator (SSPG). It jointly learns to segment words and copy entities, and outperforms existing dedicated models for 2 agglutinative languages (isiXhosa and Finnish). We investigate pretrained solutions for T2X, which reveals that standard PLMs come up short. Fine-tuning machine translation models emerges as the best method overall. These findings underscore the distinct challenge presented by T2X: neither well-established data-to-text architectures nor customary pretrained methodologies prove optimal. We conclude with a qualitative analysis of generation errors and an ablation study."
}
