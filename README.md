# Diffusion models: notes

This page contains some notes I took to learn more about diffusion models (as there have been impressive results such as [DALL-E 2](https://openai.com/dall-e-2/)).

## Important papers

* [Ho et al., 2020](https://arxiv.org/abs/2006.11239): Denoising Diffusion Probabilistic Models. Introduces DDPMs, a new class of generative models (besides others such as GANs, VAEs and normalizing flows). A neural net learns to denoise images, starting from random noise. They fix the variance, only learn the mean. They reparametrize the mean of the conditional distribution to make the neural network (a U-Net architecture) learn the noise instead.
* [Nichol et al., 2021](): Improved Denoising Diffusion Probabilistic Models. Make diffusion models achieve competitive loglikelihoods, by also learning the variance (besides the mean), improving the noise schedule (cosine instead of linear), and reducing gradient noise.
* [Dhariwal et al., 2021](https://arxiv.org/abs/2105.05233): Diffusion models beat GANs on image synthesis. Improves the neural net architecture through a series of ablations, calling the new architecture "ADM". Also introduces "classifier guidance" for conditional image generation with diffusion models. See section 2.2 of the GLIDE paper for a TLDR.
* [Ho et al., 2021](https://openreview.net/pdf?id=qw8AKxfYbI): Classifier-Free Diffusion Guidance. Make conditional image generation work without the help of a classifier, by simply replacing the class label with zeros with a certain probability during training (a bit like dropout). At inference time (during sampling), one mixes the conditional and unconditional scores.
* [Ho et al., 2021](https://arxiv.org/abs/2106.15282): Cascaded diffusion models for high fidelity image generation. Introduces a pipeline of diffusion models at progressively larger resolutions for high resolution image synthesis.
* [Nichol et al., 2021](https://arxiv.org/abs/2112.10741): GLIDE: Towards Photorealistic Image Generation and Editing with Text-Guided Diffusion Models
* [Ramesh et al., 2022](https://cdn.openai.com/papers/dall-e-2.pdf): Hierarchical Text-Conditional Image Generation with CLIP Latents (DALL-E 2)
