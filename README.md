# Meeting_Summarizer_Web
# Project Overview
This project is a comprehensive solution for transcribing, summarizing, and extracting key action items and decisions from meeting audio files. It is designed to be fully functional and runnable in Google Colab using open-source tools, avoiding API quota or billing limits.

# Features
1. Audio Transcription: Utilizes the local OpenAI Whisper (tiny) model to transcribe audio files into text efficiently with minimal resource consumption.

2. Meeting Summarization: Uses Hugging Face's BART-base model to generate concise summaries from transcripts.

3. Action Items & Key Decisions Extraction: Generates structured action items and key decisions from meetings (demonstrated with placeholder examples).

4. Participant Identification: Lists participants mentioned or speaking in the meeting.

5. Storage: Saves meeting summaries and detailed JSON reports locally for future reference.

6. User Interface: Built with Gradio to provide an interactive web UI for uploading audio files and viewing results.

7. Runs 100% free on Google Colab with no dependency on paid API keys.

# Installation Instructions
Run the following commands in Colab cells before running the main code:

bash
!pip install openai-whisper transformers sentencepiece torch gradio pydub
!apt-get install -y ffmpeg
Run the main Python script provided.

# Technical Description
1. Audio Transcription: Uses the Whisper 'tiny' model locally for robust yet lightweight transcription.

2. Summarization & Extraction: Employs a pre-trained Hugging Face transformer to create meeting summaries and generate placeholder key decisions & action items.

3. Data Models: Uses Python dataclasses to structure transcripts, summaries, action items, decisions, and participant information.

4. Storage Module: Saves summaries and metadata as JSON files for persistent storage.

5. Frontend: Gradio interface that allows users to upload audio, optionally specify language, and receive a detailed analysis report.

# Usage
1. Upload any standard audio file (MP3, WAV, M4A).

2. Optionally, specify the language code.

3. Receive an actionable meeting summary report with extracted insights.

4. Reports are saved locally for record-keeping.

# Advantages
1. Lightweight and suitable for free-tier cloud environments like Google Colab.

2. Modular and extensible design allowing easy integration of future enhancements like real-time analysis or advanced NLP tasks.

# Future Work
1. Replace placeholder action item extraction with a fine-tuned LLM.

2. Add multilingual transcription and summarization support.

3. Incorporate real-time meeting transcription and analysis.

4. Enhance user interface for batch processing of multiple meetings.
