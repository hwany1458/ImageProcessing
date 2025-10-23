# Learned Image Compression

"Learned Image Compression" is a modern approach to compressing images using machine learning techniques, typically deep neural networks, rather than traditional algorithms like JPEG or PNG.


## Overview of Learned Image Compression

Learned image compression algorithms use neural networks (often autoencoders, variational autoencoders, or generative models) to learn efficient ways to represent images with fewer bits while preserving visual quality. These models are trained end-to-end on large image datasets to optimize for rate-distortion performance (trade-off between compression rate and image quality).

### Key Concepts

 * Autoencoders: Neural networks that learn to encode input images into a compressed (latent) space, then decode them back to reconstruct the original image.
 * Entropy Coding: After encoding, additional neural networks (entropy models) predict probabilities of the representations for further bit reduction using arithmetic coding.
 * Rate-Distortion Optimization: The loss function for training balances image fidelity (distortion) and compressed size (rate).
 * End-to-End Training: The whole pipeline (encoder, quantizer, decoder, entropy model) is trained together.

### Example Workflow

 * Encoder: Compresses an image into a latent representation.
 * Quantization: Converts the latent representation to discrete values.
 * Entropy Model: Predicts probability distributions for the quantized values for efficient bit allocation.
 * Decoder: Reconstructs the image from the compressed representation.

### Popular Frameworks and Papers

 * TensorFlow Compression and CompressAI (PyTorch) provide open-source libraries for learned image compression research.
 * Notable papers:

### Demo Code Example (PyTorch-line pseudo-code)



### Applications

 * Web and mobile image delivery
 * Storage optimization
 * Video compression (extensions of learned image compression)