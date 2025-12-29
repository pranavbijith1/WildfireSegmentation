WildfireSegmentation

WildfireSegmentation is a machine learning project that detects wildfire presence in satellite imagery using a convolutional neural network (CNN). The project is built using the Kaggle Wildfire Prediction Dataset, which contains labeled images categorized as wildfire and nowildfire:
https://www.kaggle.com/datasets/abdelghaniaaba/wildfire-prediction-dataset

The model is trained on resized 32×32 RGB image patches and performs binary classification to predict the likelihood of wildfire presence. Training, validation, and evaluation are conducted using TensorFlow/Keras, with performance analyzed through accuracy curves, confusion matrices, and classification reports.

For inference on larger satellite images, the project implements a sliding-window approach that divides an image into 32×32 tiles. Each tile is independently evaluated by the trained model, and the resulting probabilities are visualized as a heatmap overlay, where higher predicted wildfire likelihoods are shown with darker red regions.

The project also includes an LLM-based analysis step, where the generated heatmap image is passed to a vision-capable language model to produce a natural-language interpretation of the detected wildfire risk patterns. This demonstrates how computer vision outputs can be combined with language models for higher-level qualitative analysis.
