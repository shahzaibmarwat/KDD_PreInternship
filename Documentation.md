Title: Training a T5 Model for Summarization on the PubMed Dataset
Objective:
The objective of this task is to train a T5 model for summarization tasks using the PubMed dataset.
Dataset:
The PubMed dataset is a large collection of scientific articles from the biomedical literature, commonly used for tasks such as text summarization and information retrieval.
•	Source: PubMed
•	Size: Dataset was split into 3 parts; Test, Train and Validate with size of 6658, 119924, and 6633 number of rows respectively.
•	Preprocessing: Before passing the dataset to the training phase, it was converted into batched tokens with the maximum size of 150, also the columns named “article” and “abstract” were removed because they were of no use during the training. Lastly, the tokenized dataset was converted into the format of pytorch tensors.
Model Architecture:
The T5 model is a transformer-based model that can be fine-tuned for various text-to-text tasks, including summarization.
•	Architecture: Transformer
•	Pretrained Model: T5
•	Fine-Tuning Objective: Summarization
Hyperparameters:
•	Learning Rate: 0.001
•	Optimizer: Adam
•	Number of Epochs: 3
Training Procedure:
•	Tokenizer: Used the T5 tokenizer to preprocess the input text and generate the target summaries.
•	Loss Function: Used the cross-entropy loss function to calculate the loss between the predicted summaries and the ground truth summaries.
