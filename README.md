# Remote-Sensing-Text-Image-Retrieval
In this thesis, we are particularly interested in text-to-image retrieval. In addition, we will explore the Arabic text-to-image retrieval to bridge the gap between the Arabic language and artificial intelligence. In particular, we propose an embedding model based on two transformer encoders a language transformer encoder and a vision transformer encoder, for English text-to-image retrieval. Then in order to increase the flexibility of the retrieval process for non-English speakers, we further fine-tune the model on descriptions from the Arabic language using single language model and bilingual model.

This project was submitted in fulfilment of the requirements for the degree of master of science in the department of computer engineering at the college of computer and information sciences - King Saud University.

## Publications: 
N. A. Alsharif, Y. Bazi, M. M. A. Rahhal, “Learning to Align Arabic and English Text to Remote Sensing Images using Transformers” 2022 Mediterranean and Middle-East Geoscience and Remote Sensing Symposium (M2GARSS).

N. A. Alsharif, Y. Bazi, M. M. A. Rahhal, “Remote Sensing Image Retrieval using Multilingual Texts” 2022 IEEE International Geoscience and Remote Sensing Symposium (IGARSS).



## Contributions: 
- We have provided two Remote Sensing (RS) text-image retrieval approaches. In both contributions, this thesis has contributed towards investigating the transformer-based backbone models for RS images. We used vision and language transformer encoders for generating visual and textual representations, respectively. We have aligned these representations by optimizing a bidirectional contrastive loss related to text-to-image and image-to-text classification.
- In the first contribution, we consider single language learning, we aligned image and English text to compare our approach to state-of-the-art methods. 
https://github.com/norahalsharif/Remote-Sensing-Text-Image-Retrieval/issues/1#issue-1275927936
![image](https://user-images.githubusercontent.com/77771990/174462480-880ea8c8-b8f0-4695-a400-69353459b1ac.png)



- In the second contribution, we proposed bilingual model to jointly learned both Arabic and English languages. In addition to learn Arabic language independently to compare single language and bilingual learning for Arabic and English languages. 
<img width="762" alt="Screen Shot 2022-02-02 at 9 59 23 PM" src="https://user-images.githubusercontent.com/77771990/174460621-8f5f6695-e6e0-437d-9b8c-fb1c857d3703.png">


- We validated the proposed approaches using three different datasets, namely Merced, RSITMD, and RSICD.



## Results: 
## First Contribution:  Cross-Modal Remote Sensing Image Retrieval using Language and Vision Transformers
In order to assess the effectiveness of our retrieval method, we compare the proposed transformer-based model and the state-of-the-art retrieval methods published recently. The results are shown for three RS text-image datasets where the best results are represented in bold. 

<img width="530" alt="Screen Shot 2022-02-02 at 9 52 38 PM" src="https://user-images.githubusercontent.com/77771990/174461434-b044784e-3e0d-4e94-8a40-2c4fbf1a0c33.png">


**Retrieval Examples with Attentions**

In this experiment, we merge all used datasets into one single dataset resulting in 15778 images. Then, we use 80% for training. Then we present some text-to-image retrieval results using random text-image pairs from the remaining 20%. In particular, we show the top six ranked images given a particular query.

<img width="550" alt="Screen Shot 2022-02-02 at 9 52 38 PM" src="https://user-images.githubusercontent.com/77771990/174461502-e420ebf9-f05a-4e9b-8f80-f4bfeeebe141.png">


**t-SNE of image and text features**

To get a global view of the resulting alignment in the feature space, the figure shows the results obtained by the t-distributed stochastic neighbour embedding (t-SNE) method for the different test text-image pairs, blue for images and red for text. We can observe that our model can effectively separate both the image and text representations into discriminative clusters with good separation boundaries, which indicates that the model can be used also for image-to-image retrieval. In addition, the visualization shows how the model attempts to align clusters from different modalities although it is challenging as we observe shifts in the clusters. We recall that a good alignment indicates the ability of a model to reduce the heterogeneity gap between the image and text representations in the common space. 
<img width="762" alt="Screen Shot 2022-02-02 at 9 56 38 PM" src="https://user-images.githubusercontent.com/77771990/174461577-27075915-3131-42c5-a30e-2af417c8c2ea.png">


## Second Contribution: Learning to Align Arabic and English Text to Remote Sensing Images Using Transformers

To assess the validity of the retrieval model on the bilingual retrieval task, we trained it independently on sentences from English and Arabic. In addition, we train it jointly on sentences from both languages

<img width="550" alt="Screen Shot 2022-02-02 at 10 08 29 PM" src="https://user-images.githubusercontent.com/77771990/174461774-ba3fd093-0e08-487c-b38d-c651c7a0a111.png">


**Visual Explain Ability**

In addition to the quantitative results, we performed another qualitative experiment to better understand the behavior of the attention mechanism employed by our transformer-based model. 

<img width="572" alt="Screen Shot 2022-02-02 at 10 14 07 PM" src="https://user-images.githubusercontent.com/77771990/174461841-b6c222cc-78ce-47c2-962c-e505474e9890.png">


**t-SNE of image and text features**

To get an intuition of how the image and the text are aligned in the joint embedding space, the figure shows the features of both the image and text obtained from the two encoders projected into the two-dimensional space using t-SNE method. 

<img width="572" alt="Screen Shot 2022-02-02 at 10 14 17 PM" src="https://user-images.githubusercontent.com/77771990/174461940-0e5a8bfd-4cb4-4cdd-bf5b-e858785cfe4d.png">




