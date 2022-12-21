# UnEnigma Machine

**Per request of a professor over concerns for academic integrity of future students the code and diagrams are not provided here, but are available upon request.**

## General Approach
The general approach which would be displayed in the python code for this project is one of statistical analysis and language detection for cryptography. 

## In detail

### Emulation
The first step  completed was to emulate a German Enigma Machine virtually. This was done in python and upon request an architecture design is available. 

### Keyspace
Next it was decided that given the key space and computation speeds of the machines available that it would be possible to propose a solution for each combination of rotors and their all respective starting positions. 

### Decryption method
The method of decryption used was hill-climbing on the plugs. The parameter that was being optimized for in hill-climbing was difference from the mean log-liklihood on unigrams, bigrams, and trigrams at varying levels of decryption. 

### Tuning 
To find hyperparameters English was scored at different levels of decryption. Log-liklihood tables for unigrams, bigrams, and trigrams were created based on text from The Communist Manifesto, and Frankenstein. After obtaining the mean scores for each level of decryption (amount of proper plugs) the standard deviation was also calculated for each level of decryption. In order to avoid throwing out the correct answer a fairly wide amount of standard deviations was set as acceptible for any given level of decryption (~2.5 sigma). Anything on the fringes of standard deviations at each level was removed all together from future processing. This siginificantly sped up decryption. 

## Result
The message was decrypted after about a month of work
