# Variational Autoencoder

VAE with Gaussian Latent Variables and Gaussian Posterior distribution.

### The approximation
The intractable p(**x**|**z**) is approximated by q_phi(**z**|**x**), c.f. mean field approximation in physics. Further possible approximations are Mises-Fisher, Gaussian Mixtures.

### References
[A high-bias, low-variance introduction to Machine Learning for physicists](https://arxiv.org/abs/1803.08823)
[A Tutorial on Variational Autoencoders with a Concise Keras Implementation](https://tiao.io/post/tutorial-on-variational-autoencoders-with-a-concise-keras-implementation/)