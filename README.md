This repository contains the supplementary material, datasets, and implementation details for our paper:

# Mask-Based-Diffusion-for-Music-Generation-From-Everyday-Sounds

- We present a generative AI method for music creation from everyday sounds using spectrogram-based diffusion.
- By adding custom masking to the Img2Img pipeline with prompt-driven style conditioning, our approach preserves input sound features while enabling flexible, fine-grained stylistic control for creative audio synthesis.
- This enables **fine-grained creative control** while preserving the input sound’s essence, resulting in versatile and stylistically coherent music synthesis.
  
<img width="854" height="394" alt="architecture" src="https://github.com/user-attachments/assets/871c70dd-197f-4938-a5d8-1e71b343c98c" />


The paper has been accepted for presentation at the 28th European Conference on Artificial Intelligence (ECAI'25).


## Resources 
#### Hugging face Model Checkpoint
[cappiepappie/riffusion-medium-600](https://huggingface.co/cappiepappie/riffusion-medium-600)

#### Colab Notebook
- [Colab notebook for music generation](https://drive.google.com/file/d/1URqlhw0f7tgZa-iFlKfyM8M7d9ptpTro/view?usp=sharing)
- [Colab notebook for training using Dreambooth by TheLastBen](https://colab.research.google.com/github/TheLastBen/fast-stable-diffusion/blob/main/fast-DreamBooth.ipynb)

## Features

- Mask-guided **spectrogram-to-music generation**.
- Custom **brightness, contrast, and downshift** parameters for creative control.
- Fine-tuned **Riffusion model** with DreamBooth for genre-specific outputs.
- Evaluation using **SSIM, Chromagram Similarity, FAD, and CLAP** metrics.

## Performance Details
All training and inference were conducted using Google Colab Pro, leveraging both NVIDIA A100 and T4 GPUs. The average inference time to generate a 5-second audio clip from a spectrogram and prompt is approximately 5-10 seconds on an T4 GPU.

## Results

- **FAD Score:** 0.570 (high perceptual similarity to human preference benchmarks).
- **CLAP Score:** 0.37 (strong semantic alignment with prompts).
- Subjective evaluation showed **high ratings for style fit, sound preservation, and music quality**.

- SSIM scores across downshift values for 65 spectrograms. Mean scores with SEM error bars (blue) show a consistent decline, highlighting the trade-off between structural preservation and generative freedom.

  <img width="850" height="552" alt="ssim_error" src="https://github.com/user-attachments/assets/a7af4cc0-9d62-421e-aca8-c7b0037bf7f7" />


- Chromagram Similarity (CENS) across downshift values for 65 spectrograms.Mean scores with SEM error bars (blue) show that low to moderate downshifts best preserve harmonic similarity, while large downshifts substantially reduce alignment with the source everyday sound
  
<img width="850" height="552" alt="cens_error" src="https://github.com/user-attachments/assets/c28e4c35-3fd9-46e8-8b41-aaebf35a06ef" />

## 🎧 Generated Audio Samples

[View here](https://cappiepappies.github.io/)

