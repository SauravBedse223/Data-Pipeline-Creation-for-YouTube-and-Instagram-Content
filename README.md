# Data-Pipeline-Creation-for-YouTube-and-Instagram-Content

#  Overview
This project aims to create a data pipeline to extract, transcribe, and format video content from YouTube and Instagram, converting it into a structured dataset suitable for further training or fine-tuning an AI model.

# Project Structure 
- main.py: The main script to run the data pipeline.
- requirements.txt: A list of Python dependencies required to run the script.
- /downloads: Directory to store downloaded video files.
- /audios: Directory to store audio files extracted from videos.
- /data: Directory to store the input and output data files.
- README.md: This file.
  
# Installation

## Clone the repository:
git clone https://github.com/SauravBedse223/Data-Pipeline-Creation-for-YouTube-and-Instagram-Content.git

## Navigate to the project directory:

cd Data-Pipeline-Creation-for-YouTube-and-Instagram-Content.git

## Install dependencies:

pip install -r requirements.tx

## Usage
Place the dataset CSV file (data.csv) containing the list of YouTube and Instagram URLs in the /data directory.

## Run the main script:

python main.py

The script will download videos, extract audio, transcribe the audio, and update the dataset with transcriptions.
The updated dataset will be saved as transcribed_data.csv in the /data directory.

# Dependencies
- youtube_dl
- instaloader
- speech_recognition
- pydub
- pandas
