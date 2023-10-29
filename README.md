# YouTube David Shapiro

This app was a proof a concept working against a RAG pipeline that we have in the works. Felt like a waste to throw it away so we're open sourcing it. It was worked on by [Gary Meehan](https://twitter.com/garmeeh) and [Sam Meehan](https://twitter.com/SamMeehan4) This is just a UI that interacts with the vector db. Just for validating our data pipeline.

In the `data` directory you will find the Whisper transcriptions of YouTube videos up to 2023-10-27. Video ids are listed in `video_ids.txt`

`whisper-youtube-transcriptions-merged.jsonl` is the dataset that was embedded. It merges the smaller whisper segments to create larger chunks. This time around it was a window of 9 with a stride of 3. (So 9 segments were merged into 1 with an overlap of 3 segments)

It uses Pinecone at the moment and Cohere to rerank the results. The UI is built with Streamlit.
