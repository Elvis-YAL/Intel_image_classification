# intel-image-classification
**Hey, guys. In this notebook, I will employ CNN to establish my preliminary model, followed by the utilization of transfer learning to construct the ultimate model. Throughout the process of employing transfer learning, I continuously fine-tuned and experimented with various pretrained models. I have diligently documented my contemplative journey, with the aspiration that it may also serve to stimulate your own reflections.**  

First of all, Let me introduce this dataset.  
This Data contains around 25k images of size 150x150 distributed under 6 categories.
{'buildings' -> 0,
'forest' -> 1,
'glacier' -> 2,
'mountain' -> 3,
'sea' -> 4,
'street' -> 5 }

The Train, Test and Prediction data is separated in each zip files. There are around 14k images in Train, 3k in Test and 7k in Prediction.  

In this notebook, I try simle CNN model and also employ some pretrained model. But I want to share my final model here.  
## MobileNet  
After testing lots of model, it seems that more basic or lightweight models perform better.  
I conducted a substantial amount of fine-tuning, including adjustments to the learning rate and experimenting with unfreezing some layers.

Here's the results. We can observe that the accuracy approaches approximately 90%.  

Next, we will visualize the evaluation results by constructing a confusion matrix. It can be noted that the model performs exceptionally well, with the only exception being its slight difficulty in distinguishing between 'buildings' and 'glacier' categories compared to the other classifications.  

 Also, I will start by randomly selecting 16 images from our validation dataset. It's evident that the model's predictions align with the actual images.

 Looks so great, we have a great result.
