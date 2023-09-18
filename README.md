# Multimodal Sentiment Analysis
- Colab Link [Click Here](https://colab.research.google.com/drive/1T3eur1IooP4pPtR2EGpSG_Aeg5cXkDCL?usp=sharing)
- Dataset Used: [Senticap](https://www.kaggle.com/datasets/prathamsaraf1389/senticap) 

# Model

This repository explores the task of multimodal sentiment analysis using text and image dual encoder i.e BERT+ResNet50. It helps to provide a holistic view of sentiment expressed in text and images.

- <b>Text+Image Neural Network: BERT + CNN </b> <br>
![Training-of-the-multimodal-CLIP-BERT-model-using-MLM-An-image-represented-by-CLIP-is](https://github.com/teamneuralnexus/multimodal-sentiment-analysis/assets/42414965/ded682a9-b2e2-4d1b-a03d-234333b78aa9)

The above image provides a rough idea about how multimodal neural networks work. Basically, the image is passed through the image encoder ( in this case ResNet50 image encoder ) and text content is tokenized and passed through text encoder ( i.e BERT ). The outputs of both the networks and concantenated and are passed through a fully connected layer. For the output we provide the no. of activations which are required to predict desired no. of labels. For our case of sentiment analysis, it's just two i.e 1 ( positive) and 0 ( negative ).

# Result

While fine tuning the model, we found out that text only model gives 99 percent accuracy on senticap eval dataset whereas the multimodal neural network almost closes to 100 percent on the eval dataset. That means that the model is understanding the data features quite accurately. Accuracy may not remain so high with other datasets as such but feeding both text and image sure shows a significant improvement over the normal text only model.

