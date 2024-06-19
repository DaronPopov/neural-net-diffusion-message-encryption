# neural-net-diffusion-message-encryption
an encrytption that uses neural networks trained on messages to communicate instructions. train at your will this is a start
# Message Encryption and Decryption using Neural Networks

## Overview

This project demonstrates a simple encryption and decryption mechanism using neural networks in PyTorch. The encryption and decryption models are implemented as neural networks, trained to transform and reverse-transform text messages into encrypted binary representations. The project includes functions to convert text to binary, split text into manageable chunks, encrypt and decrypt chunks, and process entire messages.

## Features

1. **Text-to-Binary Conversion**: Converts text messages into binary format.
2. **Chunk Splitting**: Splits text into fixed-size chunks suitable for neural network processing.
3. **Neural Network Models**: 
   - **Encryption Model**: A feed-forward neural network that encrypts binary data.
   - **Decryption Model**: A feed-forward neural network that decrypts encrypted binary data.
4. **Training Process**: Trains both the encryption and decryption models to minimize the loss between the decrypted and original messages.
5. **Full Message Encryption and Decryption**: Encrypts and decrypts entire messages by processing individual chunks.

## Installation

To run the project, you need to have Python and PyTorch installed. You can install PyTorch using pip:

```bash
pip install torch
```

## Usage

The main script trains the neural network models, encrypts a message, and then decrypts it to verify the encryption process.

1. **Define Neural Network Models**: The `EncryptionModel` and `DecryptionModel` are defined using `nn.Module` from PyTorch.

2. **Convert Text to Binary and Vice Versa**:
    - `text_to_binary_fixed(text)`: Converts text to binary format.
    - `binary_to_text(binary_str)`: Converts binary format back to text.

3. **Encrypt and Decrypt Chunks**:
    - `encrypt_chunk(encryption_model, chunk)`: Encrypts a chunk of text.
    - `decrypt_chunk(decryption_model, encrypted_chunk)`: Decrypts a chunk of encrypted data.

4. **Encrypt and Decrypt Full Messages**:
    - `encrypt_message_full(encryption_model, message_text)`: Encrypts an entire message.
    - `decrypt_message_full(decryption_model, encrypted_chunks)`: Decrypts an entire message.

5. **Train the Models and Process a Message**:
    - `train_models(message_text)`: Trains the encryption and decryption models.
    - `process_message(initial_message)`: Trains the models, encrypts a message, and then decrypts it to verify the process.

### Example Usage

Here's an example of how to use the script to encrypt and decrypt a message:

```python
initial_message = "hello what is up"
process_message(initial_message)
```

This function will output the original and decrypted messages, allowing you to verify that the encryption and decryption process works correctly.

## Future Work

- **Enhanced Security**: Improve the neural network architecture for better encryption security.
- **Variable Chunk Size**: Allow for variable chunk sizes to handle different lengths of input messages more efficiently.
- **Performance Optimization**: Optimize the training process for faster encryption and decryption.
- **Real-world Application**: Test the models on larger datasets and integrate with real-world communication systems.

## Contributing

Contributions are welcome! If you have suggestions for improvements, please open an issue or submit a pull request.
