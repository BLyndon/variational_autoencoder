# Variational Autoencoder

VAE with Gaussian Latent Variables and Gaussian Posterior distribution.

Specifications:

* Latent variable $\textbf{z} \sim p (\textbf{z}) = \mathcal N_p ({\bf\mu}, {\bf \Sigma})$, with mean zero and ${\bf \Sigma}$ diagonal
* Decoder $p(\mathbf{x}|\mathbf{z})$ is given by a MLP with a single hidden layer
* Encoder $q_\phi({\bf z}|{\bf x})= \mathcal{N}({\bf z}, \boldsymbol{\mu}({\bf x}), \mathrm{diag}(\boldsymbol{\sigma}^2({\bf x})))$
* Cost-function consisting of a reconstruction error with a regularization, that minimizes the KL-Divergence. The reconstruction error is the crossentropy between samples and their reconstructions.
* KL-Divergence for this setup
$$-D_{KL}(q_\phi({\bf z}|{\bf x})|p({\bf z}))={1 \over 2} \sum_{j=1}^J \left (1+\log{\sigma_j^2({\bf x})}-\mu_j^2({\bf x}) -\sigma_j^2({\bf x})\right).
$$

### The approximation
The intractable $p(\mathbf{x}|\mathbf{z})$ is approximated by $q_\phi({\bf z}|{\bf x})$, c.f. mean field approximation in physics. Further possible approximations are Mises-Fisher, Gaussian Mixtures.

### References
[A high-bias, low-variance introduction to Machine Learning for physicists](https://arxiv.org/abs/1803.08823)
[A Tutorial on Variational Autoencoders with a Concise Keras Implementation](https://tiao.io/post/tutorial-on-variational-autoencoders-with-a-concise-keras-implementation/)
