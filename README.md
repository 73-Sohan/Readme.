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
### Fetch and Save Voice List
Fetch the list of voices available for a specific language and save it as a JSON file:
```bash
vm.save_voice_list('./Voice_list.json')
  .then(() => {
    console.log('Voice list saved successfully!');
  })
  .catch(error => {
    console.error('Error fetching voice list:', error.message);
  });
```

Here’s a converted README.md file for your GitHub repository:

markdown
Copy code
# VoiceMaker.js _npm

VoiceMaker.js is an NPM module that offers a simple interface for creating Text-to-Speech (TTS) audio files with the Voicemaker API. You can generate TTS files in various formats, customize voice settings, and fetch the list of available voices with ease.

## Features

- Generate TTS files in formats like MP3 with adjustable parameters.
- Support for multiple languages and voices.
- Fetch and save the list of available voices for reference.
- Customize voice parameters such as speed, pitch, volume, and more.

---

## Installation

Install the package via NPM:

```bash
npm install voicemaker
Usage
Import the Module
javascript
Copy code
const vm = require('voicemaker');
Set API Key
Obtain your API key from Voicemaker and set it:

javascript
Copy code
vm.api_key('YOUR_API_KEY');
Generate TTS File
Customize the parameters and generate a TTS file:

javascript
Copy code
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
Fetch and Save Voice List
Fetch the list of voices available for a specific language and save it as a JSON file:

javascript
Copy code
vm.save_voice_list('./Voice_list.json')
  .then(() => {
    console.log('Voice list saved successfully!');
  })
  .catch(error => {
    console.error('Error fetching voice list:', error.message);
  });

### Customize Parameters
You can customize parameters individually:

```bash
vm.text('Customize your TTS parameters.');
vm.language_code('en-US');
vm.output_format('mp3');
vm.sample_rate(44100);
vm.master_pitch(5);
```
Alternatively, use the parameter object approach:
```bash
const params = {
  voice_id: 'ai3-Jony',
  language_code: 'en-US',
  text: 'This is a test for parameter-based input.',
  output_format: 'mp3',
  sample_rate: 48000,
  master_speed: 5,
  master_volume: 10,
  master_pitch: 0,
};

vm.set_params(params);
```
