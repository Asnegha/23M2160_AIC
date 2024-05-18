A Custom YOLOv2 model from scratch is implemented using pretrained YOLOv2 weights from https://pjreddie.com/media/files/yolov2.weights on pascal voc 2012 dataset.

Due to resource and compute constraints, I have fine tuned the pretrained model on Pascal VOC 2012 dataset. I have fine tuned for 1 epoch only. Model performance upon observing seems good but performance could be improved further by fine tuning for more epoch. 

### Steps to run the file
1. Run the requirements.txt file to install necessary libraries
2. Run !wget http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar to download Pascal VOC dataset. And run !tar xvf VOCtrainval_11-May-2012.tar to unzip the folder.
3. Run !wget https://pjreddie.com/media/files/yolov2.weights to download YOLOv2 pretrained weights.
4. Run OD.ipynb file for training, evaluation and inference.

### Improvements:
1. Anchor Boxes: Optimize the size and aspect ratios of anchor boxes to better match the objects in your dataset.
2. Post-Processing Techniques -- Non-Maximum Suppression (NMS): Optimize NMS parameters to reduce false positives while retaining true positives.
Soft-NMS: Use Soft-NMS which decays the detection scores of overlapping boxes rather than discarding them completely.
3. Transfer Learning approach.
4. Parameter fine tuning.
5. Explore different loss function.

### Reference:
1. https://fairyonice.github.io/Part_1_Object_Detection_with_Yolo_for_VOC_2014_data_anchor_box_clustering.html
