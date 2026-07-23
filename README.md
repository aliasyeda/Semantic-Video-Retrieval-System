# Semantic Video Retrieval System
### Multimodal Video Search using CLIP & FAISS

<img width="2048" height="1152" alt="Semantic Video Retrieval System - Hero Banner 2" src="https://github.com/user-attachments/assets/693eb442-cf61-4666-9616-5113b8e4a4cc" />

## Overview

Semantic Video Retrieval System is a proof-of-concept multimodal AI application that enables natural language search across multiple video files.

Instead of relying on filenames or manually browsing videos, the system understands the semantic content of video frames using OpenCLIP embeddings and retrieves the most relevant frames for a user’s text query.

Each search result includes the matching frame, source video, and timestamp, allowing users to quickly locate relevant moments within a collection of videos.

---

## Features

- Natural language video search
- Multi-video indexing
- Automatic frame extraction using OpenCV
- CLIP-based semantic image embeddings
- FAISS vector similarity search
- Source video identification
- Timestamp retrieval
- End-to-end pipeline implemented in Google Colab

---

## System Architecture

```
Input Videos
      │
      ▼
Frame Extraction (OpenCV)
      │
      ▼
Image Embeddings (OpenCLIP)
      │
      ▼
FAISS Vector Index
      │
      ▼
Text Query
      │
      ▼
CLIP Text Embedding
      │
      ▼
Similarity Search
      │
      ▼
Top Matching Frame
+ Source Video
+ Timestamp
```

---

## Technology Stack

- Python
- OpenCV
- PyTorch
- OpenCLIP
- FAISS
- NumPy
- Pillow
- Matplotlib
- Google Colab

---

## Dataset

This project was evaluated using a small collection of publicly available sample videos for proof-of-concept testing.

To reproduce the project, create a `videos/` directory and place your own `.mp4` files inside it before running the notebook.

---

## How It Works

1. Upload one or more video files.
2. Extract frames at regular intervals using OpenCV.
3. Generate semantic embeddings for each frame using a pretrained OpenCLIP model.
4. Store embeddings in a FAISS vector index.
5. Convert a natural language query into a CLIP text embedding.
6. Perform similarity search against indexed frame embeddings.
7. Return the most relevant frame together with its source video and timestamp.


---

## Running the Project

1. Create a folder named `videos`.
2. Place your own `.mp4` files inside the folder.
3. Run the notebook from top to bottom.
4. Enter a natural language query (e.g., "person", "cat", "kitchen") to retrieve the most relevant frames.

---

## Example Queries

- person
- bicycle
- cat
- kitchen
- girl
- walking
- cooking

---

## Challenges Encountered

- Selecting an appropriate frame sampling interval to improve retrieval quality.
- Managing Python package dependencies in Google Colab.
- Handling runtime resets and regenerating embeddings after notebook restarts.
- Extending the pipeline from single-video retrieval to indexing and searching across multiple videos.

---

## Future Improvements

- Clip-level retrieval instead of frame-level retrieval.
- Evaluation on larger egocentric video datasets.
- Interactive Streamlit web interface.
- Retrieval accuracy evaluation using benchmark queries.

---

## Project Outcome

This project demonstrates the complete workflow for multimodal semantic video retrieval using pretrained vision-language models and vector similarity search.

The implementation highlights practical applications of CLIP embeddings, FAISS indexing, and natural language search for efficient exploration of video content.


## Designed, Developed & Documented by :
## Syed Alia Samia
