# p2p-secure-sound-json-transfer
Transferring JSON from phone to phone(s) through sounds. And encrypt the characters before transferred as sound. fExperiments to see if it will work.

## Issue #1 - Generating, playing, receiving and checking sounds

[Idea](https://github.com/eklem/sound-json-transfer/issues/2):

**Transmitting end:**

* Set to transmitting mode
* Initially, play i.e. the 10 frequencies to be used so receiver can adjust to listening to the bits/bytes
* Create a checksum of JSON stringified
* Transform JSON to numbers
* Then play the numbers

**Receiving end:**

* Set to receiving mode
* Listen to 10 frequencies and find the average of each
* Some error-checking if 10 wasn't found
* Listen to JSON stringified
* Transform to JSON stringified
* Create checksum so users can check if JSON transfaered is okay
* Transform to JSON

Part of the work will be to see how many different tones it is possible to transfer. Maybe also make it possible to define. Lowest level would be just bits, zeroes and ones.

How to generate tones and play them:
https://stackoverflow.com/questions/39200994/how-to-play-a-specific-frequency-with-javascript

## Issue #2 - Encrypting the sounds

If issue 1 works, try to [encrypt the sounds](https://github.com/eklem/sound-json-transfer/issues/2)
