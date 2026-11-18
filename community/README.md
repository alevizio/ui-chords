# Community loops

Loops made with ui-chords. Each one has two files:

- `<name>.mp3`, the app's own Download MP3.
- `<name>.json`, what was played: the settings, then every key pressed in each take. That's enough to play the loop again, so it could also be how the app saves loops.

| Loop | By | What it is | Key, tempo |
| --- | --- | --- | --- |
| [Sobremesa](sobremesa.mp3) | [alevizio](https://github.com/alevizio) | Lo-fi neo-soul. FM piano with a root bass, boom-bap drums and a bell melody | F major, 84 BPM, 4 bars |
| [Juntada](juntada.mp3) | [alevizio](https://github.com/alevizio) | Warm house. Four on the floor, a saw arpeggio, a pad and a square hook with a 1/8 delay | A minor, 122 BPM, 4 bars |

## The JSON

- `settings` is the same object the app saves in the browser under `ui-chords:settings`.
- `adjust` is the grid Adjust snapped every take to (4, 8 or 16), or `false` when it was off.
- `takes` are recorded in order, one loop light each. When a take has its own `settings`, they change the app's settings right before that take and stay for the ones after it.
- In `notes`, `beat` counts from the start of the take, four to a bar. `key` is the key from 1 to 7, `len` is how many beats it's held, and `dir` is the joystick (`up`, `up-right`, `right`, `down-right`, `down`, `down-left`, `left` or `up-left`), left out when it's centered. Drum hits have no `len`: keys 1 to 7 are kick, clap, snare, hat, tom, rim and open hat.

Both loops were recorded on the app's own looper with Adjust at 1/16. A small script read each JSON and pressed the keys on the beat.

## Add yours

Play a loop, download the MP3 and open a pull request that adds it here with a row in the table. The JSON is optional.
