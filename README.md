# Recall: Local RAG Knowledge Assistant

A small retrieval-augmented knowledge assistant that runs entirely in the browser. No backend, no API keys, and your documents never leave your machine.

## How it works
1. **Ingest**: add text or `.txt` / `.md` files to the library.
2. **Chunk**: documents are split on sentence boundaries into passages of a configurable length.
3. **Index**: passages are tokenised (stop-word removal, light stemming) and indexed for BM25 ranking.
4. **Retrieve**: the question is scored against every passage and the top results are returned.
5. **Answer**: the most relevant sentences from the best passages are assembled into a short answer, each tagged with its source passage.

## Tuning
Two controls make it easy to see how configuration affects relevance: **passage length** (retrieval granularity) and **passages shown** (top-k). Relevance bars and highlighted query terms show why each passage was chosen.

## Preview
See `recall-preview.mp4` for a short walkthrough.

## Stack
HTML, CSS and vanilla JavaScript. Open `index.html` to run it.

## Notes
The original pipeline used OCR to ingest scanned documents. This browser build focuses on the retrieval and answering workflow and accepts text input.
