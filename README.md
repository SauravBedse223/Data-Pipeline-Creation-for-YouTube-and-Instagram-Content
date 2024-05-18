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

  # Requirments
- ## Import Libraries:
   The script imports necessary libraries including youtube_dl, instaloader, speech_recognition, pydub, pandas, and os.

- ## Function Definitions:

- download_youtube_audio(url, output_path): Downloads audio from YouTube videos using youtube_dl.
- download_instagram_video(url, output_path, username): Downloads videos from Instagram using instaloader. It requires a valid Instagram session, which is loaded from a saved file.
- transcribe_audio(audio_path): Transcribes audio using Google's Web Speech API provided by speech_recognition.
- convert_to_wav(input_audio_path, output_audio_path): Converts audio files to WAV format using pydub.
  
## Main Function (main()):

- Loads the dataset from a CSV file.
- Creates output directories for downloaded videos and audio files.
- Specifies the Instagram username for session loading.
- Iterates through each row in the dataset:
- Determines the type of video (YouTube or Instagram) based on the URL.
- Downloads the video and extracts audio. If there's any error, it continues to the next row.
- Checks if the video was downloaded correctly and if not, tries to find the downloaded video file in the output directory.
- Converts the video to WAV format if necessary.
- Transcribes the audio. If there's any error during transcription, it handles it and sets the transcription as "Transcription failed."
- Updates the dataset with the transcription result.
- Saves the updated dataset to a new CSV file.
  
## Execution: 
The main() function is called if the script is executed directly.
  
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
