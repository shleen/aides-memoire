## Convolutional Neural Networks (CNNs)

Input: three-dimensional matrix (e.g. images)

### Why CNNs?
CNNs are referred to, commonly, as automatic feature detectors. For example, give it a group of images of dogs & it can learn that dogs have, for example, 2 ears & a nose. All of this is done with back-propagation.

### Some models to look at
- R-CNN
- Fast R-CNN
- Faster R-CNN
- SSD
- **YOLO**
 
### YOLO (Redmon et al.)
Currently the best model (fastest & most accurate)

The evolution of YOLO
- YOLO
- YOLO v2
- YOLO 9000
- YOLO v3

#### The idea
Divide an image into SxS grid of cells. 
Each cell in the grid predicts B bounding boxes.
Each cell can only contain one object. (called the one-object rule)

Each bounding box contains
- x co-ordinate of top left corner
- y co-ordinate of top left corner
- width of the box
- height of the box
- confidence that an object exists in the box

Each cell contains
- probability distibution of class confidences (e.g. what are the chances that this box contains a human? or a dog?)

Rather than using randomly-generated bounding boxes, though, we can pre-define several anchor boxes (that roughly approximate the shape of certain classes of object). Then, we predict the offset from this anchor boxes to find the bounding boxes of the object. These anchor boxes are called *priors*. This means that we're now looking for the center of the box, not the left corner.

#### Training
2 phases.

Train a classifier on ImageNet. Expose it to IMAGES. Remove the fully connected layer (the last part). Just keep weights for a baseline for object detection.

Loss functions- optimization!

Input- 416 x 416 images only!

### Detection vs Classification
**Classification**- typically one image input, one prediction output
**Detection**- also one image input, but multiple prediction outputs

## Common Datasets
- Common Objects in Context (COCO)

Probably the larget dataset for labelled images. Check it out [here](cocodataset.org)!

- PASCAL

The best. Before COCO. Find it [here](host.robots.ox.ac.uk/pascal/VOC)

- Imagenet 

Used to train the best image classifiers & object detectors. Find it [here](www.image-net.org)
