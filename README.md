# Visual Storyteller

## Project Description
This project is an image captioning system that generates a text description for an input image. The goal is to combine computer vision and natural language processing so that the model can understand the contents of an image and describe them using a sentence.

The project uses a pretrained ResNet18 model to extract image features and an LSTM network to generate captions word by word.

## Dataset
The project uses the Flickr8k dataset.
Around 8000 images
Each image has 5 different human-written captions

The dataset is used to train the model to learn the relationship between images and their descriptions.

## Project Files
`data_and_training.ipynb` – loads the dataset, preprocesses the data, trains the model, and saves all required files.
`inference.ipynb` – loads the trained model and generates captions for images.
`models/` – contains the saved model, vocabulary, configuration, and training history.

## Model
The model consists of two parts.

The first part is a pretrained ResNet18 network that extracts a feature vector from each image. The last classification layer is removed because only the visual features are needed.

The second part is an LSTM network. It receives the image features together with the previous words of the caption and predicts the next word until the caption is finished.

## How to Run
1. Place `caption_data.zip` in the project folder.
2. Open `data_and_training.ipynb` in Jupyter Notebook and run all cells from top to bottom. This will train the model and save the required files in the `models` folder.
3. After training is complete, open `inference.ipynb` and run all cells. The notebook loads the saved model and generates captions for sample images.

## Libraries
This project uses:

Python
PyTorch
Torchvision
NumPy
Pandas
Matplotlib
Pillow
Scikit-learn
tqdm

## Results
The model is able to generate reasonable captions for many images, especially those containing common objects or activities such as people, dogs, bicycles, sports and outdoor scenes.
Some captions are not completely correct especially for more complex images with multiple people or uncommon situations. This is expected because image captioning is a difficult task and the model uses a relatively simple encoder-decoder architecture.

Overall the model demonstrates that it can learn meaningful relationships between images and natural language captions.