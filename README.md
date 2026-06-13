# The Visual Storyteller

This is my final project for image captioning. The main idea of the project is to build a model that takes an image as input and generates a short caption for it.

For example, if the input image shows a dog running outside, the model should generate a sentence like:

```text
A dog is running in the grass.
```

## Project Overview

In this project, I work with both images and text. The model has to understand what is shown in an image and then describe it using natural language.

This task is interesting because it combines two areas of deep learning:

* computer vision
* natural language processing

The computer vision part helps the model understand the image, and the language part helps the model generate a sentence.

## Dataset

The project uses the provided dataset called `caption_data.zip`.

The dataset contains:

* 8,000 images
* 5 human-written captions for each image

The dataset is not uploaded to this GitHub repository because it may be too large. To run the notebooks, `caption_data.zip` should be placed in the main project folder.

## Notebooks

### data_and_training.ipynb

This notebook contains the main development and training process.

It includes:

* loading the images and captions
* cleaning and preprocessing the captions
* preparing the vocabulary
* preparing the image transformations
* defining the image captioning model
* training the model
* saving the trained model files

### inference.ipynb

This notebook is used to test the trained model.

It includes:

* loading the saved model
* defining the `generate_caption(image_path, model)` function
* testing the model on images
* showing successful generated captions
* showing failure cases
* explaining where the model works well and where it makes mistakes

## Model Idea

The project uses an encoder-decoder idea.

The encoder looks at the image and extracts important visual features.
The decoder uses these features to generate the caption word by word.

In simple words:

```text
Image → Encoder → Image features → Decoder → Caption
```

## How to Run

1. Install the required libraries:

```bash
pip install -r requirements.txt
```

2. Put `caption_data.zip` in the main project folder.

3. Run the training notebook:

```text
data_and_training.ipynb
```

4. After the model is trained and saved, run the inference notebook:

```text
inference.ipynb
```

## Author

Anastasia Gelashvili
