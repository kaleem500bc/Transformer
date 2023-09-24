# Overview
Implementation of transformer model for language modeling. It also contain implementation of a language model that is trained on a text dataset and can generate new text.

- **Transformer Architecture**: It consists of multiple attention heads, feedforward layers, and layer normalization. The architecture is highly customizable through `parameters.yaml`.

- **Custom Dataset**: Define a custom dataset for training, allowing to adapt the model to different types of text data.<br>
The model is trained on a text dataset provided by Udacity. You can download it using the following command:

```bash
wget -O "dataset.txt" "https://raw.githubusercontent.com/udacity/deep-learning/master/tensorboard/anna.txt"
```

## Configuration

Before using the code, make sure to configure the hyperparameters in the `parameters.yaml` file:

```yaml
hyperparameters:
  learning_rate : 1e-3
  dropout : 0.1
  size_of_attention_head : 4
  num_of_attention_head : 4
  n_embd : 64
  batch_size : 1024
  block_size : 256

training:
  epochs : 600
  patience : 10
  model_checkpoint_path : "language_model.pt"

dataset:
  dataset_file_name : "dataset.txt"

max_new_tokens : 100
