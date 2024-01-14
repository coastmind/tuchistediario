# TuChisteDiario

Visit our tiktok with the content created.

<a href="https://www.tiktok.com/@tuchistediario">
<img src="etc/tiktok.webp" width="50">
</a>

### Authors:
* [Álvaro Beltrán Camacho](https://www.linkedin.com/in/alvarobeltrancamacho/)
* [Jesús Periñán Dávila](https://www.linkedin.com/in/jesus-perinan-davila/)

## Introduction

This project presents an innovative approach to automate the creation of TikTok videos that feature animated avatars telling jokes. The process harnesses the power of several cutting-edge artificial intelligence (AI) models, each contributing uniquely to the production of engaging and entertaining content. 

### Overview of the Process

1. **Voice Generation with Bark**: Initially, the project utilizes the Bark model to convert text-based jokes into realistic and expressive voiceovers. Bark is renowned for its ability to generate natural-sounding speech, making it an ideal choice for creating the audio layer of the TikToks.

2. **Subtitle Generation with Whisper**: Following the voice generation, Whisper is employed to transcribe the spoken jokes into subtitles in the `.srt` format. Whisper's advanced speech recognition capabilities ensure accurate and timely subtitles, enhancing the accessibility and understanding of the content.

3. **Avatar Animation with SadTalker and DALL-E 3**: The next phase involves animating avatars using SadTalker, which are then brought to life with visuals created by DALL-E 3. DALL-E 3 excels in generating unique and expressive avatars based on text descriptions, while SadTalker provides the animation framework to make these avatars narrate the jokes in a lifelike manner.

4. **Video Editing and Subtitle Integration with MoviePy**: Finally, the project leverages MoviePy for video editing tasks, including the integration of subtitles. MoviePy is a flexible tool that allows for seamless merging of the audio, animated visuals, and subtitles, culminating in the final TikTok-ready video.

## Technologies Used

- **Bark**: An AI model for generating human-like voiceovers from text. [Learn more about Bark](https://github.com/suno-ai/bark).
- **Whisper**: A state-of-the-art speech recognition system for creating accurate subtitles. [Learn more about Whisper](https://github.com/openai/whisper).
- **SadTalker**: An animation tool designed for bringing avatars to life in a realistic manner. [Learn more about SadTalker](https://github.com/OpenTalker/SadTalker).
- **DALL-E 3**: An advanced AI model by OpenAI for generating creative and detailed images from text descriptions. [Learn more about DALL-E 3](https://openai.com/dall-e-3).

## Architecture

The architecture is based on google drive as file system and notebooks running on google colab in chain. These notebooks generate different files in the google drive folders that will be used by the following notebooks.

<image src="etc/tuchistediario architecture.drawio.png" alt="Arquitecture">

## Instalation Guide

1. Copy `TuChisteDiario` folder into your google Drive.
2. Open notebooks with google colab.

## User Guide

Into the file `chistes_con_metadatos.csv` you will find all jokes to execute this project. Its important to know about `audio_creado` `video_creado` `subs_creado` columns this columns will control generated jokes.

1. Execute `Bark.ipynb` notebook to generate an audio into `audios_chistes` folder. This notebook will generate masculine and femenine audios with `.srt` subtitles. When audio and subtitle are generated, `audio_creado` column is set to True.
2. Execute `SadTalker.ipynb` notebook to generate videos from avatars and audios. When video is generated, `video_creado` column is set to True.
3. Execute `createSubtitles.ipynb` notebook to add subtitles to your generated video. When video with subtitles is generated, `subs_creado` column is set to True.

## Examples

[![Example](https://img.youtube.com/vi/7JaV9-eCPTQ/mqdefault.jpg)](https://www.youtube.com/shorts/7JaV9-eCPTQ)


