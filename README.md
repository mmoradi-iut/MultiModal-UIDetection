# MultiModal-UIDetection
A multi-modal UI control detection model based on YOLO and LLM-generated textual descriptions.

In this repository, you can find information, results, data, and source codes of the multi-modal user interface control detection model. The method and experiments are described and discussed in the paper titled "Multi-modal user interface control detection using cross-attention".

<h2>Multi-modal user interface control detection model</h2>
<p>The following image illustrates the overal architecture of the YOLO model that serves as the basis of our multi-modal detection model:</p>
<br>
<img width="800" src="https://github.com/mmoradi-iut/MultiModal-UIDetection/blob/main/Figure-1.jpg">

<p>The following image illustrates the overal architecture of the neck part of our multi-modal detection model. The Backbone remains as same as the YOLOv5 model.</p>
<br>
<img width="400" src="https://github.com/mmoradi-iut/MultiModal-UIDetection/blob/main/Figure-6.jpg">

<h2>Cross-attention modules</h2>
<p>The first fusion method is <b>element-wise addition</b>, where each element in the attended feature tensor is simply added to the corresponding element in the image feature tensor. This approach is computationally efficient and straightforward to implement, with no additional parameters introduced during merging.</p>
<br>
<img width="400" src="https://github.com/mmoradi-iut/MultiModal-UIDetection/blob/main/Figure-3.jpg">

<p>The second fusion method is <b>weighted sum</b>, where learnable scalar weights are assigned to both the attended and image features before summation. These weights are trained jointly with the rest of the model, allowing it to dynamically adjust the importance of visual and textual inputs during training.</p>
<br>
<img width="400" src="https://github.com/mmoradi-iut/MultiModal-UIDetection/blob/main/Figure-4.jpg">

<p>The third fusion method is <b>convolutional fusion</b>, where the attended and image features are first concatenated along the channel dimension and then passed through a convolutional layer. This approach allows the model to learn complex, non-linear interactions between the two modalities and adaptively integrate them at each spatial location.</p>
<br>
<img width="400" src="https://github.com/mmoradi-iut/MultiModal-UIDetection/blob/main/Figure-5.jpg">

<h2>Dataset</h2>
<p>The dataset contains 16,155 UI screenshots, each annotated with bounding boxes and corresponding class labels. We split the dataset into a training set of 14,155 images and a test set of 2,000 images, with 10% of the training set (1,416 images) used as a validation set during training. The dataset includes 23 distinct UI control classes, representing a wide range of interface components such as buttons, icons, input fields, and charts.</p>

In order to have access to the datasets and get the permision, send an email to m.moradi-vastegani@tricentis.com.
