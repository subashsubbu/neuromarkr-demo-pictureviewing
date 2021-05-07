# Background
- This demo was bootstrapped with [notion-react-starter](https://github.com/neurosity/notion-react-starter). Logging in to the EEG headset device is handled via the card in the upper right - once the device is authenticated, it should automatically be sensed every time the user opens the web app.
- Viewing affective (emotion-laden) pictures elicits attentionional processes [(Schupp et al., 2003)](https://doi.org/10.1111/1469-8986.3720257). For example, depending on the pleasantness or affective intensity of a picture, such attentional changes may be measured using electroencephalogram, whereby stimulus-evoked event-related brain responses (e.g., the "Late Positive Potential") are typically larger for highly emotional (e.g., chocolate cake, cute puppy dog, erotica) than low emotional (e.g., stapler, kitchenware) images.
- The picture viewing "task" was designed using ```lab.js```'s [experiment builder](https://labjs.felixhenninger.com/), and draws images from the [Open Affective Standardized Image Set (OASIS)](https://doi.org/10.3758/s13428-016-0715-3) (**WARNING: explicit content**). The sequence and collection of images are meant to be exemplars, which may be supplemented or replaced by other sequence timings, image sets, etc. 
- The raw EEG "brainwave" data generated throughout the task is printed to the console in JSON format by ```console.log()``` after all pictures have finished being presented.

# Outstanding issues
- Presently, the raw "brainwaves" data bundle that is generated by the Neurosity headset goes nowhere; posting this data to a server database is ideal.
- As of Fall, 2020, ```lab.js``` does not enable callbacks for each stimulus events (the only callbacks supported are ```prepare```, ```run```, ```end```, and ```commit```), making it impossible to inject markers via notion-js's ```addMarker``` capability. Adding markers would be ideal for this event-related potential measurement project, but for the moment the recordings are simply "bookended" at the task start and end times, and events must be matched up using the ```lab.js``` output CSV file. An alternative library that DOES support event callbacks is [jsPsych](https://www.jspsych.org/overview/callbacks/).


# Getting Started
- npm install
- npm start
- 
