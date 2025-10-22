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
