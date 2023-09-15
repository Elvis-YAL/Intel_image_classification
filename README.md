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
![download](https://github.com/Elvis-YAL/intel-image-classification/assets/40426433/d931fb94-c7a1-4213-9dd2-fbea48a87610)

In this notebook, I try simle CNN model and also employ some pretrained model. But I want to share my final model here.  
## MobileNet  
After testing lots of model, it seems that more basic or lightweight models perform better.  
I conducted a substantial amount of fine-tuning, including adjustments to the learning rate and experimenting with unfreezing some layers.

Here's the results. We can observe that the accuracy approaches approximately 90%.  
![download](https://github.com/Elvis-YAL/intel-image-classification/assets/40426433/21832eb6-7b5d-49f0-8323-d2306749ae16)

Next, we will visualize the evaluation results by constructing a confusion matrix. It can be noted that the model performs exceptionally well, with the only exception being its slight difficulty in distinguishing between 'mountain' and 'glacier' categories compared to the other classifications.  
![download](https://github.com/Elvis-YAL/intel-image-classification/assets/40426433/b831c3f4-6979-49a1-95b3-dad5662fbcbf)

 Also, I will start by randomly selecting 16 images from our validation dataset. It's evident that the model's predictions align with the actual images.  
 
![download](https://github.com/Elvis-YAL/intel-image-classification/assets/40426433/78e59abf-eac1-4680-a974-1ff4c6796747)

 Looks so great, we have a great result.
