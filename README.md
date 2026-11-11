# Intune: AI Piano Melody Generation

A Python prototype that trains an LSTM on encoded monophonic music sequences and samples new note and rest events into a MIDI file. The project uses `music21`, NumPy, and TensorFlow/Keras.

## Project files

- `preprocess.py` — reads the configured Kern corpus and encodes note sequences.
- `train.py` — trains and saves the sequence model.
- `melodygenerator.py` — samples a sequence and writes MIDI output.
- `display.py` — displays generated music data.

## Setup

Use Python 3 and install `numpy`, `music21`, and `tensorflow` in a virtual environment. From the repository root, run:

```bash
python -m venv .venv
# Activate the environment, then:
python -m pip install numpy music21 tensorflow
```

The preprocessing script expects the Kern corpus at `deutschl/zuccal` (see the path configured in the script). Create the `dataset/` directory before preprocessing. Then run the preprocessing, training, and generation scripts from the repository root. The pipeline writes model and MIDI artifacts locally.

## Status

This is an experimental learning project. Model quality depends on the source corpus and training setup; generated output is not evaluated as a production composition system.
