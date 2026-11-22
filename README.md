# Voice of Wolaita Recorder

A browser page for recording people reading Wolaytta sentences, to build
speech-recognition training data. Open it on a phone or laptop:

**https://teddy-2004.github.io/wolaita-recorder/**

- Each speaker gives consent on screen (research use required, public
  release optional). No names are stored.
- Recordings stay in the browser on that device until you tap
  **Export all as zip**. Nothing is uploaded to this site.
- `prompts.txt` holds the sentences to read, one per line
  (`id<TAB>sentence`). They are training-split transcripts from the
  [WAXAL](https://huggingface.co/datasets/google/WaxalNLP) Wolaytta corpus
  (CC-BY-4.0, Google Research); no sentence from its validation or test
  split is included.

Exports are merged into the dataset with
`python -m wal_data merge-recordings` in the wolaytta-asr-data project.
