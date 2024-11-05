# S2S-Bench
[中文版](./README_zh.md)

Welcome to our project! This project primarily focuses on the reproduction and evaluation of Speech Large Models (SLMs), particularly speech-to-speech (S2S) models that support both speech input and output. This repository consists of three parts:
* 1) Reproduction code for various models;
* 2) Arena web code for testing and demonstration;
* 3) Test datasets.

In existing research, benchmarks for evaluating model instruction-following capabilities often overlook paralinguistic information in both input and output and lack direct comparison of speech output across models. To address this, we propose an innovative arena-style S2S benchmark covering multiple real-world tasks, using the ELO rating system for comparative analysis. Preliminary experiments indicate that while some models perform better on knowledge-intensive tasks, they still face significant challenges in expressive speech generation. This research provides critical insights for the development of S2S models and establishes a robust framework for evaluating model performance across semantic and paralinguistic dimensions.

## Model Reproduction
### Cascade Model
The Cascade Model consists of three main components: ASR-LLMs-TTS
* We use `whisper-large-v3` as the ASR tool;
* We use `gpt-4o-2024-08-06` (text version) as the LLM tool;
* We use `CosyVoice-300M-Instruct` as the TTS tool.

The code can be found in [./CascadeModel](./CascadeModel).

To run this code smoothly, you need to set up environments for each of the three components separately.

#### Whisper-ASR
For ASR tool configuration, refer to the [Whisper model card on Hugging Face](https://huggingface.co/openai/whisper-large-v3).

#### GPT4o-LLMs
To configure the LLMs, please use the following command:
```shell
pip install openai==0.28.0
