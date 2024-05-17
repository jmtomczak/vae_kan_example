# An example of parameterizing VAEs with Kolmogorov-Arnold Nets (KANs)
A simple example of VAEs parameterized with KANs.

### Some results
Some results in terms of the ELBO (in brackets: the number of parameters):
- `MLP` (~0.5M): 96.8
- `KAN` (~4M): 97.2
- `MLP+KAN` (~2.7M): 96.7
- `KAN+MLP` (~1.6M): 97.5
- `KAN (enc) and MLP (dec)` (~1.2M): 96.9

where:

- `MLP` denotes a VAE fully parameterized with MLPs.
- `KAN` denotes a VAE fully parameterized with KANs.
- `MLP+KAN` denotes a VAE parameterized by MLP with a KAN layer on top (both for the encoder and the decoder).
- `KAN+MLP` denotes a VAE parameterized by KAN layers with a Linear layer on top (both for the encoder and the decoder).
- `KAN (enc) and MLP (dec)` denotes a VAE with a KAN-based encoder and an MLP-based decoder.
