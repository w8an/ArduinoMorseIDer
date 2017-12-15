# ArduinoMorseIDer
Written in Visuino openwire development environment.<br>
Steven R. Stuart, W8AN

### Usage
**Programming**<br>
Morse code is manually entered into the Value property of the TextValueMorse object. Begin your message with a 0. Use 1 for tone, 0 for silence. The letter 'A' (di-dah) would be encoded as 101110. A dot (10) then a dash (1110). Use two zeros (00) for an inter-word space and four zeros (0000) to separate words. So 'hi world' which sounds like this: di-di-di-dit &nbsp; di-dit &nbsp; &nbsp; di-dah-dah &nbsp; dah-dah-dah &nbsp; di-dah-dit &nbsp; di-dah-di-dit &nbsp; dah-di-dit, would be encoded as:
```
 H         I       W           O           R         L            D
 * * * *   * *     *  -   -    -   -   -   *  -  *   *  -  * *    -  * * 
0101010100010100000101110111001110111011100101110100010111010100011101010
```

- Set Morse code speed in the Frequency property of the CodeSpeed object.
- Set Morse code audio frequency in the Initial Frequency property of the PlayFrequency object.
- Set message launch interval time using the Frequency property of the PulseGenerator object. Note that the PulseGenerator Frequency property is in Hertz (pulses per second). If you want a message started every 20 seconds, input 0.05 (1/20 Hz). Once per minute would be 0.016667 (1/60 Hz).

**Using an Arduino Nano**<br>
- Pin D12 is the transmitter switch output, D13 is an inverted output
- Pin D8 is a switched morse code output
- Pin D4 is morse code audio. Use a 10uf capacitor in series with a speaker running to GND to hear the code.

