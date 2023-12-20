# Interview.ai

**TL;DR: AI interviews you, on whatever topics you want, creating audio archives and transcripts.**

## Motivation

This project is to scratch a personal itch: have an AI interview me, to get me to talk about topics I want to share with the world. Also to explore AI a bit, and hopefully release something useful for others as well as myself.

## Quickstart

- install [llm](https://github.com/simonw/llm)
- install [ospeak](https://github.com/simonw/ospeak)

```bash
cp .env.example .env   # and edit as needed
pip3 install -r requirements.txt
./interview.py
```

## Features

Initial release will be purely CLI based workflow - no GUI, nerds only :)

- [x] Create context (YAML config file):
  - [x] Description of interviewee
  - [x] List of topics to talk about
  - [x] System prompt describing interviewer characteristics
- [x] AI Interviewer asks question about a topic
  - Generated by LLM based on context above
- [x] Speak question out loud to interviewee
  - Ideally record audio, although we can reconstruct it later (in higher quality) from the text
- [ ] Save question as text
- [ ] Record audio of interviewee answering question
- [ ] Transcribe interviewee audio to text
  - realtime or higher quality? probably start with realtime, for better interview flow
  - whisper.cpp?
  - transcribe_demo.py?
- [ ] User hits spacebar to indicate answer complete, ready for next question
- [ ] Feed text back to interviewer as part of "chat" flow, to generate next question
