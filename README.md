# ArduinoMorseIDer
Written in Visuino openwire development environment.
Steven R. Stuart, W8AN

### Usage
Morse code is manually entered into the TextValueMorse object. Begin your message with a 0. Use 1 for tone, 0 for silence. The letter 'A' (di-dah) would be encoded as 101110. A dot (10) then a dash (1110). Use two zeros (00) for an inter-word space and four zeros (0000) to separate words. So 'hi world' which sounds like this: di-di-di-dit &nbsp; di-dit &nbsp; &nbsp; di-dah-dah &nbsp; dah-dah-dah &nbsp; di-dah-dit &nbsp; di-dah-di-dit &nbsp; dah-di-dit, would be encoded as:
```
  H        I   Sp  W          O            R         L           D
0101010100010100000101110111001110111011100101110100010111010100011101010
```

- Set Morse code speed in Frequency property of CodeSpeed object.
- Set Morse code audio frequency at Initial Frequency property of PlayFrequency1 object.
- Set message delay time using Interval property of Delay1 object.

Using an Arduino Nano
- Pin D2 is the transmitter switch output
- Pin D8 is a switched morse code output
- Pin D7 is morse code audio. Use a 10uf capacitor in series with a speaker running to GND to hear the code.

