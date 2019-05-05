# tp-midiout-lite
Customized versions of ledfyr's "ab-midiout-lite" project

These sketches are based on ledfyr's ab-midiout-lite https://github.com/ledfyr/ab-midiout-lite
Which is based on Trash80's Arduinoboy project https://github.com/trash80/Arduinoboy

The MIDI Thru code was taken from Send MIDI IN to MIDI OUT (THRU)
by P.J. Drongowski
http://sandsoftwaresound.net/arduino-midi-sequencer-testing/

Some changes apply to all versions:
- MIDI THRU added
- Automatic transport Start/Stop messages have been removed
- Manual transport Start/Stop messages have been added:
  - Y6E = Start
  - Y6F = Stop
  - Note: This eats up the last 2 possible Program Change values

Version-specific changes:

**OMNI**
- All LSDJ channels are set to MIDI Channel 1
- Using X6y to change MIDI channels is disabled
- All special commands are moved up on number, e.g.
  - X0y = MIDI CC 1 (scaled)
  - X1y = MIDI CC 2 (scaled)
  - X2y = MIDI CC 3 (scaled)
  - X3y = MIDI CC 7 (scaled)
  - X4y = Velocity (scaled)
  - X5y = Set Tempo/Tap Tempo
  - X6y = Chords
  
