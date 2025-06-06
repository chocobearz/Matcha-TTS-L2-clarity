<div align="center">

# The additon of a clarity mode for:
# 🍵 Matcha-TTS: A fast TTS architecture with conditional flow matching

### See the original repo [here](https://github.com/shivammehta25/Matcha-TTS)

[![python](https://img.shields.io/badge/-Python_3.10-blue?logo=python&logoColor=white)](https://www.python.org/downloads/release/python-3100/)
[![pytorch](https://img.shields.io/badge/PyTorch_2.0+-ee4c2c?logo=pytorch&logoColor=white)](https://pytorch.org/get-started/locally/)
[![lightning](https://img.shields.io/badge/-Lightning_2.0+-792ee5?logo=pytorchlightning&logoColor=white)](https://pytorchlightning.ai/)
[![hydra](https://img.shields.io/badge/Config-Hydra_1.3-89b8cd)](https://hydra.cc/)
[![black](https://img.shields.io/badge/Code%20Style-Black-black.svg?labelColor=gray)](https://black.readthedocs.io/en/stable/)
[![isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)

<p style="text-align: center;">
  <img src="https://shivammehta25.github.io/Matcha-TTS/images/logo.png" height="128"/>
</p>

</div>

> Through several psychoacoustic and lingustic experiments we have added a `clarity` mode to Matcha-TTS that, this clarity mode has been validated for first language speakers in noise and for second language speakers. It was found to improve their comprehension of
> difficult vowels by up to 30%. This work is specific to tense lax vowel pairs, e.g. peel/pill, pool/pull, not, nut. future work will expand it other parts of clarity.

>  Another addition on Matcha-TTS is direct play mode, where the TTS will directly play the audio file, rather than simply writing a .wav file, useful for end-to-end applications


## Installation

1. Create an environment (suggested but optional)

```
conda create -n matcha-tts python=3.10 -y
conda activate matcha-tts
```

2. Install Matcha TTS from source

```bash
pip install git+https://github.com/chocobearz/Matcha-TTS-L2-clarity
cd Matcha-TTS
pip install -e .
```

3. Run CLI

```bash
# This will download the required models
matcha-tts --text "<INPUT TEXT>" --clarity
```

or open `synthesis.ipynb` on jupyter notebook adding the clarity flag

### CLI Arguments

- To synthesise from given with clarity text, run:

```bash
matcha-tts --text "<INPUT TEXT>" --clarity
```

- To synthesise from a file, run:

```bash
matcha-tts --file <PATH TO FILE> --clarity
```

- To batch synthesise from a file, run:

```bash
matcha-tts --file <PATH TO FILE> --batched --clarity
```

Additional arguments

- Speaking rate

```bash
matcha-tts --text "<INPUT TEXT>" --speaking_rate 1.0 --clarity
```

- Sampling temperature

```bash
matcha-tts --text "<INPUT TEXT>" --temperature 0.667 --clarity
```

- Euler ODE solver steps

```bash
matcha-tts --text "<INPUT TEXT>" --steps 10 --clarity
```

- Direct playback

```bash
matcha-tts --text "<INPUT TEXT>" --clarity --play
```

> For information on training and other information and ways to run the model please see the original Matcha-TTS repo
