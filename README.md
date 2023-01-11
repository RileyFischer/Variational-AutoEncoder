This is my attempt to make a Variational-Autoencoder(VAE) from scratch. Variational autoencoders are probabilistic generative models that use neural networks to encode and decode something such as an image. The benefit of VAE's is that they allow for information to be stored at a smaller size after the data has been encoded. If we have found a decoder that does a good job then we can return our data to its original state using the decoder with minimal information loss.

From the output of the notebook, it is shown that this VAE does a good job at creating a good encoder and decoder that can first simplify the image to a few features and then bring the image back to its original state with a small amount of loss of information. After just a few epochs we see that the VAE can correctly recreate the correct number and also write the number with a similar handwriting.


Input:
![image](https://user-images.githubusercontent.com/55674235/211691119-2287de43-6ac5-46ea-9763-907fb9e7221a.png)

Output of VAE:
![image](https://user-images.githubusercontent.com/55674235/211691155-60a0c3fd-882a-4736-9bdd-aaf185ceb214.png)


What makes the Variational AutoEncoder different than other auto encoders is that it tackles the problem of the latent space irregularity by making the encoder return a distribution over the latent space instead of a single point and by adding in the loss function a regularisation term over that returned distribution in order to ensure a better organisation of the latent space.
