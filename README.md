# Seq2Seq Model
This repository contains code for a Seq2Seq (Sequence-to-Sequence) model implemented using Keras. The model is designed for neural machine translation, translating sentences from one language to another.

## Dataset
The model is trained on the spa-eng dataset, which consists of sentence pairs in Spanish and English. The dataset is loaded from the file located at `C:\path-to-dr\spa-eng\spa.txt`. The number of samples used for training is specified by the NUM_SAMPLES parameter.

## Model Architecture
The Seq2Seq model architecture consists of an encoder-decoder framework. The encoder utilizes LSTM (or CuDNNLSTM) layers to process the input sequence and generate a fixed-length representation. The decoder, also equipped with LSTM (or CuDNNLSTM) layers, takes the encoded representation as input and generates the translated output sequence. The model incorporates word embeddings from pre-trained GloVe word vectors to enhance the representation of words in both the input and output sequences.

## Training
During training, the model optimizes its parameters using the Adam optimizer. A custom loss function is employed to handle sequences appropriately. The training process is performed for a specified number of epochs (EPOCHS) with a batch size of BATCH_SIZE. The training loss and accuracy are recorded and plotted to monitor the model's progress.

## Inference
The trained model can be used to make translations. The model is saved as s2s.h5. To generate translations, an input sentence in the original language is encoded using the trained encoder model, and the decoder model generates the translated sentence.

To try out some translations, run the code and enter 'Y' when prompted to continue. The model will randomly select an input sentence from the dataset and provide the translation.
