# Image-encryption-using-Chaotic-Map
# Image Encryption using Chaotic Maps and XOR

This repository implements an encryption and decryption scheme for grayscale images using chaotic maps and XOR operations. The method leverages the properties of chaotic maps to generate pseudo-random sequences that are used to scramble and obfuscate the pixel positions of the image, followed by an XOR operation to enhance security.

## Features

- **Chaotic Map-Based Scrambling**: Utilizes an extended logistic map to generate a pseudo-random sequence for pixel scrambling.
- **XOR-Based Encryption**: Applies XOR between the pixel values and a generated key stream for an additional layer of security.
- **Encryption and Decryption**: Supports both encryption and decryption of grayscale images, making it easy to secure and retrieve your data.
- **Custom Key Generation**: The method allows you to generate a key stream using a seed, ensuring that the encryption is reproducible with the same seed.

## How It Works

1. **Image Scrambling**: The grayscale image is first scrambled using a chaotic map. This reorders the pixel positions based on the generated chaotic indices.
2. **XOR Operation**: The scrambled image is then XORed with a key stream. This key stream is generated using a pseudo-random number generator seeded for reproducibility.
3. **Decryption**: The decryption process is the reverse. The XOR operation is applied again to the encrypted image with the same key stream, followed by descrambling using the reverse of the chaotic map indices.

### Extended Logistic Map

The extended logistic map is defined as:

Xn+1 = u ∗ Xn ∗ (1− Xn)

This generates a chaotic sequence of values that are used to scramble the pixel positions of the image.

### XOR Encryption

XOR is a common operation used in cryptography. The pixel values are XORed with a key stream to provide additional security. The same key stream is required for decryption.

## Usage

### Prerequisites

- Python 3.x
- `Pillow` library for image processing
- `NumPy` library for numerical operations

Install the required libraries using pip:

```bash
pip install pillow numpy