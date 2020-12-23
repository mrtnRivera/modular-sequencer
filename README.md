# The Modular Sequencer

![Example](https://github.com/mrtnRivera/modular-sequencer/blob/main/img/mod_seq%20example.png)

A Pure Data sequencer designed for modularity.
The Modular Sequencer is a simple abstraction for creating rhythmic patterns. It can output MIDI notes or in-patch bangs.

Just copy "mod_seq.pd" and "mod_seq-help.pd" where your patches can find them and create your sequencers with **[mod_seq]**.

## Controls

* On/Off toggle - Turn the sequence On or Off.
* steps - Set the number of steps for the sequence. min: 1, max: 32
* ms - Time interval between events in milliseconds.
* note - Change every MIDI note in the sequence to a given note.
* rand - Create a random rhythmic pattern, MIDI notes stay the same.
* ch - Set the MIDI channel for sending notes.
* MIDI toggle - Toggle MIDI output in this object.
* Note toggles - Activate a MIDI note and bang event in the sequence.
* MIDI note values - Set a MIDI note for each sequence event.


## Inlets:

* On/Off - A bang (or number) sets the toggle to On if it's Off and the other way around.
* Steps - Set the number of steps in the sequence.
* ms - Set the time interval between events in milliseconds.
* Tempo - Set the time interval between events in bpm.
* Note - Set the MIDI note for each step.
* Random - A bang creates a random rhythmic pattern.

## Outlets:

* Outlets 1 to 8 - Outputs a bang when the corresponding step is on and the sequence is running.
* Outlet 9 - Outputs a bang when the sequence is running and any given step is on.