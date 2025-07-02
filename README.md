# My Data Science Project
In this project, which is the Masters Thesis of Moritz Stockmar, the usage of parliamentary speeches by the 'Alternative für Deutschland' (AfD) on Social Media, namly TikTok, Instagram (Reels) and YouTube (Shorts), is analyzed. The main objective is to learn which speeches (and excerpts thereof) are used by the AfD and what differentiates them from the population of all of AfD's speeches.

## Overview
The Thesis, which has not been graded yet, can be accessed on demand. Just write me. In short the method of this research project is as follows.

Firstly, the raw data is acquired. For the parliamentary data this is done via an API for the [DIP](https://dip.bundestag.de/). The short videos on the other hand are not downloaded automatically. I selected the ones dipicting parliamentary proceedings by hand and downloaded them with [yt-dlp](https://github.com/yt-dlp/yt-dlp). The raw data is not included in this repository and can also be accessed on demand. 

After that, some preprocessing is done to de-duplicate the short videos and build a corpus out of all AfD speeches held during the 20th legislative period of the Bundestag. 

The analysis itself is done regarding four dimensions of the data. Firstly, some meta-data of the speech excerps is analysed (e.g. who are the most depicted speakers). Secondly, the themes of the speeches are analysed using pretrained BERT-based ML-models as well as self-made dictionaries for classifying speeches (on sentence level). These models are all open source and accessible via huggingface. The self-made dicitionaries are included in this repository.
Thirdly, the emotionality of the speeches (e.g. senitment and hate-speech) is analysed and lastly, some linguistic clues for populist communication are searched.

In conclusion, the analysis shows that the short videos are more populist in severel theoretically derived metrics (see the Thesis) or in other words, that the AfD behaves like one might expect from a rational acting right-wing populist actor.

## Installation
The whole code is in an Jupyter Notebook and can should be run more or less in order. This is especially important for the preprocessing parts of the code.

### Prerequisites
Software:
- The code was written for Python 3.12.9 and not tested for any other version
- Everything from environment.yaml
- ffmpeg 

Hardware:
- at least 6 GB of VRAM for Whisper

## License
This project is licensed under the MIT License. 