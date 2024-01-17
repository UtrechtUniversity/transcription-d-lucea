# Transcription D-LUCEA

This GitHub repository contains the code used to transcribe parts of the Database of the Longitudinal Utrecht Collection of English Accents (D-LUCEA) using WhisperAI speech-to-text. The main aim was to enable the transcription of only relevant parts of each recording. Additionally, the repository includes scripts for processing the transcripts to enhance their usability for the subsequent corpus analysis using regular expressions in python.

## Getting Started

Clone this repository to get a copy on your PC.

`git clone https://github.com/UtrechtUniversity/transcription-d-lucea.git`

### Prerequisites

To install and run this project you need to have the following prerequisites installed.

- ffmpeg
- pandas
- librosa
- soundfile
- whisper
- whisperX

It is recommended to use a GPU powered computer (or server) for creating transcripts. With a recent GPU you can produce transcripts using the state-of-the-art Whisper models in a few seconds. At UtrechtUniversity you can get access to a VRE with a GPU via [RDM support](https://www.uu.nl/en/research/research-data-management/tools-services/software-and-computing/virtual-research-environments).

### Installation

We recommend using Conda to create a Python environment for this project.  
First follow the [setup instructions for WhisperX](https://github.com/m-bain/whisperX#setup) to create an environment.

Additionally install Whisper and ffmpeg using the [setup instructions for Whisper](https://github.com/openai/whisper#setup)

Lastly, install librosa and soundfile using pip:
```
pip install librosa
pip install soundfile
```
And on a Linux operating system, you will need to install `libsndfile` to work with `soundfile`:

```
sudo apt-get install libsndfile1
```

### Project structure

When reading data files, the scripts are assuming the project structure below; the scripts use relative paths so should run out-of-the-box if you use the same structure:

```
.
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
├── src              <- main folder for all source code
│   └── trim_and_transcribe.ipynb
├── data             <- All project data, not published in git
│   ├── audio_files
│   ├── trimmed_audio
│   └── Recordings.xlsx         
└── output
    └── transcripts
```

## Usage
The jupyter notebook that is used for creating transcripts can be found in the `src/` folder.

## About the Project

**Date**: Month Year

**Researcher(s)**:

- Name of researcher 1 (researcher.1@uu.nl)
- Name of researcher 2 (researcher.2@uu.nl)

**Research Software Engineer(s)**:

- Name of RSE 1 (rse.1@uu.nl)
- Name of RSE 2 (rse.2@uu.nl)

### License

The code in this project is released under [MIT license](LICENSE).

### Attribution and academic use

## Contributing

Contributions are what make the open source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

To contribute:

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Contact
