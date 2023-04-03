# voice-assistant
Voice assistant demo using whisper on device and gpt-3.5-turbo

## Details
* google text to speech(gtts) used for text to speech

## Limitations
* The text to speech runs on the device where the notebook is run so it is not suitable for deployment as constructed 

## Observed problems
* On the first recording, the actual audio recording seems to be slow to start often.  1 second or so behind clicking the button.

## Tested on
* Windows Subsystem for Linux(WSL) Ubuntu 20.04.5 LTS
* RTX 3070 mobile system

## Setup
**Note that this install includes more dependencies than are strictly necessary for running this notebook.**
**This is because I copied a previous environment that I had as the starting environment**
* install the conda package manager if you do not have it
* `git cloneclone https://github.com/c1505/voice-assistant.git`
* `cd voice-assistant`
* `conda env create -f environment.yml`
* Install the conda environment your environment as a jupyter kernal
	* `python -m ipykernel install --user --name voice-assistant --display-name "voice-assistant"`
* create a file named `.env` in the root of your repository
* add your open ai api key to that file like `OPENAI_API_KEY=`

## Run
* Launch jupyter `jupyter lab`
* Choose the `voice-assistant` environment
* Open and run the voice_assistant.ipynb notebook
* click "record from microphone" in the gradio app
* if everything works, you should hear an audio response from your computer
and the full text transcription of the input and the text of the output

# Future directions
* play resulting text to speech audio through the browser
* get working as a gradio demo that can be hosted on hugging face or elsewhere
* one of:
    * set up the same functionality on a smart speaker
    * set up the same functionality on an android app