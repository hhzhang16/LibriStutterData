# LibriStutterData
LibriStutter data for a class final project. Putting it here so that we can access 
it with our Colab. Will remove after the project ends!

Note: This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License. 
License here: https://creativecommons.org/licenses/by-nc/4.0/
We are not modifying the dataset or using it for commercial purposes.

NOTE 2: We had to remove all examples alphabetically after 7780 (so 78 and onwards) as 
the annotations stopped matching up with the audio for some reason.

LibriStutter Dataset
======================
Queen's University

Tedd Kourkounakis
tedd.kourkounakis@queensu.ca
======================

1. General information
----------------------
The Libristutter dataset is a synthesized dataset comprised from the public LibriSpeech 
ASR corpus. It contains artificially stuttered speech, as well as time-aligned transcriptions
and stutter classification labels for 5 stutter types. It was created for the use of 
classification of stuttered speech. It was generated using 20 hours of audio selected
from the 'dev-clean-100' section of the original corpus, consisting of "clean" speech.

All corresponding metadata, including speaker, book, and chapter information
are provided in the original public LibriSpeech ASR corpus.

2. Structure
----------------------
Each annontation CSV file contains information pertaining to the corresponding
FLAC file of the same name, provided in the public LibriSpeech ASR corpus.

Eg. The '130-1240-0000.csv' annotation file provides annotations for the 
'130-1240-0000.flac' audio file.


2.1 Structure of Audio
----------------------
All audio files are represented as FLAC files, and are all found within the 
'LibriStutterAudio' folder. The organizational (folder) structure is the same
 as used in the original public LibriSpeech ASR corpus, as follows:

For the file 'LibriStutterAudio/130/1240/130-1240-0000.flac',
130 corresponds the speaker ID
1240 corresponds to the chapter read by the speaker
0000 corresponds to the prompted phrase within the chapter read by the speaker

2.1 Structure of Annotations
----------------------
All annotation files are represented as CSV files, and are all found within the
'LibriStutterAnnotation' folder. These annotation files maintain similar 
organizational (folder) structure as their corresponding audio files.

Eg. The 'LibriStutterAnnotation/130/1240/130-1240-0000.csv' annotation file will
have its corresponding audio file located in
'LibriStutterAudio/130/1240/130-1240-0000.flac'.

Each annontation CSV file contains information pertaining to the corresponding
WAV file of the same name, provided in the UCLASS Release Two dataset.

Eg. The 'F_0101_10y4m_1.csv' provides annotations for the 'F_0101_10y4m_1.wav' file.

Each row in each annotation file pertains to a single word or sound utterance, and
its corresponding timing and labels. The information for each row is as follows:

Column 1: 	Word transcriptions as provided by the LibriSpeech ASR corpus. Note
		that values containing 'STUTTER' denote the location of one of 5 added
		stutter types.

Column 2:	Time (in seconds) when utterance begins.

Column 3:	Time (in seconds) when utterance ends.	

Column 4:	Label classifying utterance as clean speech, or one of 6 stutter types.
	0: 	clean
	1: 	interjection
	2: 	sound repetition
	3: 	word repetition
	4: 	phrase repetition
	5: 	prolongation
