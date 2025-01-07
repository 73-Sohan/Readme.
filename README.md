# voiceMaker_npm
Voicemaker.js  is an NPM module that offers a simple interface for creating `Text-to-Speech`  (TTS) audio files with the Voicemaker API. 

## Features

- Generate TTS files in formats like MP3 with adjustable parameters.
- Support for multiple languages and voices.
- Fetch and save the list of available voices for reference.
- Customize voice parameters such as speed, pitch, volume, and more.

## Installation

Install the package via NPM:
```bash
npm install voicemaker
```

### Import the Module
```bash
const vm = require('voicemaker');
```
### Set API Key 
Obtain your API key from Voicemaker and set it:
```bash
vm.api_key('YOUR_API_KEY');
```
### Generate TTS File
Customize the parameters and generate a TTS file:
```bash
vm.text('Hello, this is a sample text-to-speech conversion!');
vm.voice_id('ai3-en-US-Mike');
vm.master_speed(0);    // Speed range: -100 to 100
vm.master_volume(5);   // Volume range: -100 to 100

vm.tts_file('output.mp3')
  .then(() => {
    console.log('TTS file created successfully!');
  })
  .catch(error => {
    console.error('Error:', error.message);
  });
```
