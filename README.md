# Solar Panel Detection on Colab.
This repository demonstrates an example of a TensorFlow Lite model re-trained on colab for solar panel detection. Sample size is 50 with a 15:35 split for testing and training, respectively. 

### A workflow of re-training deep learning models acquired from TensorFlow Hub.

1. Create labeling data.
2. Convert Geotiff files *(with coordinates)* to JPG files(without coordinates).
3. Generate a XML file *(with XY pixels and bounding boxes)* for each TIFF file from a TXT that locates the position of each point and denotes its corresponding polygon and TIFF file.
4. Arrange a TensorFlow-used data format:
  - Split all JPG files to two folders, "train" and "test".
  - Convert the corresponding XML files to a single CSV file in the folder "train" and "test", respectively.
  - Generate the corresponding TFRecord files named as "train.record" and "test.record".
5. Re-train the model:
  - Select a model from TensorFlow Hub.
  - Manually modify the content of "pipeline.config".
  - Re-train and export.
6. Perform inference on testing dataset and calculate metrics for validation.
7. Ready to be applied to real-world data!



In closing, I'd like to acknowledge the assistance of @x1001000 in this project.
