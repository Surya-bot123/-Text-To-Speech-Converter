# Text to Speech Converter

A simple and elegant web-based Text to Speech Converter. This web application allows users to type any text and listen to it using various voice options. It uses the Speech Synthesis API available in modern web browsers.

## Table of Contents

1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [How to Use](#how-to-use)
4. [How it Works](#how-it-works)
5. [Screenshots](#screenshots)
6. [Contributing](#contributing)
7. [License](#license)
8. [Acknowledgements](#acknowledgements)

## Features

- **Text Input**: Type any text you want to be converted into speech.
- **Voice Selection**: Choose from available voices in your browser.
- **Listen Button**: Click the button to hear the text read aloud.
- **Responsive Design**: The application is fully responsive and works across devices like desktop and mobile.

## Tech Stack

- **HTML**: Structure of the web page.
- **CSS**: Styling of the page to make it look good and user-friendly.
- **JavaScript**: Implements the logic for text-to-speech functionality using the Speech Synthesis API.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/text-to-speech-converter.git
2. Navigate to the project directory:
```
cd text-to-speech-converter
```
3. Open the ``` index.html ```file in your preferred web browser.
4. Open the index.html file in your preferred web browser.
5. Select the voice from the dropdown.
6. Click the "Listen" button to hear the text read aloud.

## How it Works
The Text to Speech Converter project uses the Web Speech API to convert text input by the user into speech. Here's a detailed breakdown of how the application works:
1. #### Speech Synthesis API

* The core of the text-to-speech functionality comes from the Speech Synthesis API provided by modern web browsers. The Speech Synthesis API allows your application to speak text aloud using synthetic voices. This is part of the Web Speech API, which is supported by most modern browsers (like Chrome, Firefox, Safari, etc.).
#### Key steps:
* We create an instance of ``` SpeechSynthesisUtterance ```. This is an object that represents the text you want to speak.
* The ``` SpeechSynthesisUtterance ``` object has properties such as ``` text ```,``` rate ```, ``` pitch ```, and ``` volume ```, which control the speech's characteristics. In this project, we mainly focus on the text property, which contains the text the user types.
* Once the text is set on the ``` SpeechSynthesisUtterance ```object, we use ``` window.speechSynthesis.speak() ``` to read the text aloud.
#### Example Code:
```
let speech = new SpeechSynthesisUtterance();
speech.text = "Hello, welcome to the Text to Speech Converter!";
window.speechSynthesis.speak(speech);
```

2. #### Voice Options
Different browsers support different voices. Some browsers may have multiple voices (e.g., male, female, different languages), while others may have just one default voice.
* When the page loads, we use the ``` speechSynthesis.getVoices() ``` method to get a list of all available voices.
* The ``` voices ``` array contains voice objects that provide details like the name, language, and gender of each voice.
* The user can select a voice from a dropdown menu. When the user selects a voice, the ``` speech.voice ``` property is updated to the selected voice.
#### Example Code:
```
let voices = window.speechSynthesis.getVoices(); 
speech.voice = voices[0];  // Default to the first voice
```
* We populate the dropdown menu with available voices, so the user can select one.
3. #### User Interaction (UI Elements)
The user interacts with the app through the following UI elements:
* **Textarea**: The user types the text they want to be converted to speech.
* **Voice Dropdown**: This dropdown lets the user choose from different available voices (if supported by the browser).
* **Play Button**: The user clicks this button to trigger the text-to-speech conversion and hear the text read aloud.
#### Example of Button Action:
```
document.querySelector("button").addEventListener("click", () => {
speech.text = document.querySelector("textarea").value;  // Get the text from the textarea
window.speechSynthesis.speak(speech);  // Speak the text
});
```
* This event listener listens for a click on the "Listen" button, then sets the text of the ``` SpeechSynthesisUtterance ``` object to the content of the textarea. Finally, it calls ``` window.speechSynthesis.speak(speech) ``` to read the text aloud.
4. #### Customization: 
Users can customize the voice selection from the dropdown. The voice options include different languages, genders, and accents (depending on browser support). 




### Explanation of the Structure:
1. **Project Title**: At the top, we have the title of the project — "Text to Speech Converter".
2. **Features**: Describes the key functionalities of the application.
3. **Tech Stack**: Lists the technologies used to build the project (HTML, CSS, JavaScript).
4. **How to Use**: Provides step-by-step instructions on how to use the application locally.
5. **How it Works**: Describes the technical details of how the text-to-speech feature functions.
6. **Screenshots**: Optional section where you can add a screenshot of the project if desired.
7. **Contributing**: Invitation for others to contribute to the project.
8. **License**: Information about the open-source license under which the project is available.
9. **Acknowledgements**: Credits to any libraries or tools used in the project (e.g., Speech Synthesis API, font).

Feel free to edit the content based on your preferences, and add relevant images or details as necessary.



## Screenshots

![website Screenshots](![Image](https://github.com/user-attachments/assets/123df8b9-6fd4-4943-9106-1f6dc00419f3)
![Image](https://github.com/user-attachments/assets/fdc0c67f-aa62-4c82-bcfc-17a7e1228cdc)
![Image](https://github.com/user-attachments/assets/8ff083a2-2527-4635-b2b5-44214cf36138)



## Contributing
If you'd like to contribute to this project, feel free to fork the repository, create a branch, and submit a pull request. Any improvements or bug fixes are welcome!


## Acknowledgements
* Speech Synthesis API – Used for the text-to-speech functionality.
* Poppins Font – The font used in this project.

