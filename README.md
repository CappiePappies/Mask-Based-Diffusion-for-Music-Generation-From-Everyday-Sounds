# Mask-Based-Diffusion-for-Music-Generation-From-Everyday-Sounds
- We present a generative AI method for music creation from everyday sounds using spectrogram-based diffusion. 
- By adding custom masking to the Img2Img pipeline with prompt-driven style conditioning, our approach preserves input sound features while enabling flexible, fine-grained stylistic control for creative audio synthesis. 
- This enables **fine-grained creative control** while preserving the input sound’s essence, resulting in versatile and stylistically coherent music synthesis.

The paper has been accepted for presentation at the 28th European Conference on Artificial Intelligence (ECAI'25).

This repository contains the supplementary material, datasets, and implementation details for our paper:

##  Features

* Mask-guided **spectrogram-to-music generation**.
* Custom **brightness, contrast, and downshift** parameters for creative control.
* Fine-tuned **Riffusion model** with DreamBooth for genre-specific outputs.
* Evaluation using **SSIM, Chromagram Similarity, FAD, and CLAP** metrics.


##  Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/<your-repo-name>.git
cd <your-repo-name>
pip install -r requirements.txt
```


##  Repository Structure
WE CAN CHANGE LATER 
```
├── data/                # Preprocessed datasets (everyday sounds, music clips)
├── notebooks/           # Jupyter notebooks for training & evaluation
├── src/                 # Core implementation (masking, diffusion, evaluation)
│   ├── mask_generation.py
│   ├── diffusion_pipeline.py
│   ├── evaluation.py
├── results/             # Generated outputs & evaluation logs
├── README.md            # Project documentation
```

---

##  Datasets


---

##  Usage

Example: generate music from an input sound + prompt

```python
from src.diffusion_pipeline import MusicGenerator

gen = MusicGenerator()
gen.generate(
    input_sound="data/sounds/clock.wav",
    prompt="lofi hip hop",
    output_path="results/clock_lofi.wav",
    brightness=0.05,
    contrast=200,
    downshift=40
)
```


##  Results

* **FAD Score:** 0.570 (high perceptual similarity to human preference benchmarks).
* **CLAP Score:** 0.37 (strong semantic alignment with prompts).
* Subjective evaluation showed **high ratings for style fit, sound preservation, and music quality**.

( add graphs here ) 
---

##  Supplementary Material

* Paper (ECAI 2025): \[arXiv link / DOI once available]
* Dataset & Code Release: \[Zenodo DOI once published]



✨ *This work demonstrates a new direction in spectrogram-based music generation, combining feature retention with flexible style adaptation for creative audio synthesis.*
