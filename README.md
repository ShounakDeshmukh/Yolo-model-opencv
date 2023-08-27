# Yolo-model-opencv
Yolo v3 implemented in Opencv for static images

There is a Python Notebook demonstrating object detection

## Moving on to functions which need to be ported to rust
### Preprocessing:

`cv2.resize` - To Resize images
    - Could be exposed via any image manipulation crate

`cv2.dnn.blobFromImage` - convert image to blob for CV2
  - Very convoluted matrix transform and concatenation could be written from scratch

`cv2.dnn.readNet` - Loads graph structure + pre-trained weights
    - Under the hood reads the binary representaion of the graph and assigns weights could be challenging

### Utility Functions:
`cv2.imshow`
`cv2.draw` - All drawing geometry

