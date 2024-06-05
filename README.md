# Video Processing and Multi-Modal Retrieval

This project demonstrates how to process a YouTube video to extract images, audio, and text, and then build a multi-modal index for retrieving relevant images and context based on a query. The final response generation uses GPT-4 for reasoning the correlations between the input query and augmented data.

## Table of Contents

- [Project Overview](#project-overview)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [License](#license)

## Project Overview

This project includes the following steps:
1. Downloading a YouTube video.
2. Extracting images and audio from the video.
3. Converting the audio to text.
4. Building a multi-modal index using the extracted images and text.
5. Retrieving relevant images and context based on a query.
6. Generating a response using GPT-4.

## Setup Instructions

### Prerequisites

- Google Colab account
- GitHub account
- OpenAI API key (for GPT-4)

### Steps

1. **Clone the repository**:

    ```bash
    git clone https://github.com/imranajec/video-processing-multimodal-index.git
    cd video-processing-multimodal-index
    ```

2. **Open the Jupyter Notebook**:

    Upload `Video_Processing_and_Multimodal_index.ipynb` to your Google Colab and open it.

3. **Set the OpenAI API key**:

    Ensure you have your OpenAI API key saved in Google Colab's user data:

    ```python
    import os
    from google.colab import userdata
    OPENAI_API_TOKEN = userdata.get('OPENAI_API_KEY')
    os.environ["OPENAI_API_KEY"] = OPENAI_API_TOKEN
    ```

4. **Run the notebook**:

    Follow the steps in the notebook to process the video and perform multi-modal retrieval.

## Usage

1. **Download and Process the Video**:
    - The notebook will download the specified YouTube video, extract images and audio, and convert the audio to text.

2. **Build the Multi-Modal Index**:
    - The extracted images and text are used to build a multi-modal index using LanceDB.

3. **Query the Index**:
    - A query is run against the index to retrieve relevant images and context.

4. **Generate a Response**:
    - GPT-4 is used to generate a response based on the retrieved images and context.

## Dependencies

The following Python libraries are required:

```plaintext
llama-index-vector-stores-lancedb
llama-index-multi-modal-llms-openai
llama-index-embeddings-clip
llama-index-readers-file
llama_index
openai-whisper
lancedb
moviepy
pytube
pydub
SpeechRecognition
ffmpeg-python
soundfile
torch
torchvision
matplotlib
scikit-image
ftfy
regex
tqdm
