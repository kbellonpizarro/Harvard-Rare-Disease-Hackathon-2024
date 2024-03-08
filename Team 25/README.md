# Scanning Speech Enhancer App Functionality

## Start page of app

| Transcribe text |		| Record audio message |

### Record audio message
This is the speech-to-speech functionality.
The patient records what they want to say, and our tool modifies it by removing pauses between syllables and increasing the speed of the speech. In future releases, more advanced speech enhancement can be incorporated, using signal processing and/or machine learning, to enhance speech that specifically comes from HOD ataxic speech.  The result is an audio recording that can be sent in a messaging app or to a physician. There can be the option for the message to come with a text transcription, which would feed the enhanced voice recording to an existing text-to-speech service.
	The patient presses the start button to start taking audio input, or the stop button to end the recording (giving the option to save or send it). After stopping, there should be options to listen to the past 10 or 5 seconds of the recording, and to rerecord the past 10 or 5 seconds, and this will delete the last 10 or 5 seconds of the first recording and enable the user to immediately start recording again. Our program will splice the two together into a single result recording, so that the user can continue where they left off in the original recording, minus where a mistake was made.

### Transcribe text
The phone is meant to be shown to the person the patient is talking to
Text appears on the phone as the patient is speaking. Unlike traditional text-to-speech applications, this does not use pauses to calculate when the end of a word is: it accumulates syllables until it detects the start of the next word using context, and then combines the previous syllables into a word.

### Preset messages
The user of the app can save preset messages for frequent use. Such as “Hi my name is ___, I have a disorder called HOD which affects my movements and coordination.” or their address or phone number. This could include audio, text or both, and could be manually uploaded or typed. (Assuming these messages are for frequent use and don’t need to be updated frequently, the patient can upload them with the help of a caregiver).

### Relevant Literature
https://www.sciencedirect.com/science/article/pii/S0006899319302252?via=ihub#b0535
https://hodassoc.org/ - background on HOD
https://rarediseases.org/gard-rare-disease/hypertrophic-olivary-degeneration/
https://www.frontiersin.org/journals/neurology/articles/10.3389/fneur.2017.00302/full - has a good diagram of the olivary nuclei and the cerebellum 
https://en.wikipedia.org/wiki/Scanning_speech - Scanning Speech
https://www.verywellhealth.com/scanning-speech-5272531
https://www.youtube.com/watch?v=kYP7ICsFyV4&t=43s - video used in presentation



