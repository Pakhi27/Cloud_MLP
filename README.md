# **Cloud-Based Multimodal Language Processing System**

## Team Members
- **Pakhi Singhal** – 22BDS042  
- **Ravi Raj** – 22BDS051  
- **Preethi Varshala S** – 22BDS045

## Project Overview

This project presents a powerful cloud-enabled multimodal language processing system, integrating cutting-edge AI services to handle translation, text-to-speech (TTS), speech-to-text (STT), and image captioning in a unified, user-friendly web platform. Leveraging Google Cloud's robust APIs for language and speech processing alongside a BLIP model (via Hugging Face) for image captioning, the system showcases real-time, scalable, and intelligent cross-modal communication. Deployed using modern cloud platforms (Netlify for frontend and Render for backend), it delivers high availability, responsiveness, and modularity, making it ideal for applications in e-learning, assistive technology, and content generation.



## Methodology

### Architecture
The system adopts a decoupled architecture:
- **Backend:** Python Flask RESTful API
- **Frontend:** React.js SPA (Single Page Application)

This separation enhances scalability, independent development, and seamless CI/CD deployment.

### Development Workflow
All services (text, speech, image) are modularized across backend and frontend layers to improve flexibility, maintainability, and testing. The AI functionalities are accessed via secure, optimized endpoints.

### Key Components

#### Flask Backend
- Lightweight and extensible Python framework
- Integrates with Google Cloud APIs and local machine learning models
- Handles audio/image uploads, API routing, error handling, and inference processing

#### React Frontend
- Intuitive, responsive, and cross-device compatible
- Supports live feedback, drag-and-drop uploads, and dynamic content rendering

#### Cloud & AI Services
- **Google Cloud APIs** for Translation, TTS, and STT
- **Hugging Face Salesforce BLIP** model hosted locally for fast, rich image captioning



## Deployment Strategy

### Frontend (Netlify)
- **Platform:** Netlify (static hosting)
- **CI/CD:** Auto-deployment via GitHub integration
- **Build Settings:** `npm run build` with publish directory `build/`
- **Env Config:** `REACT_APP_API_URL` dynamically set for backend API
- **Live Demo:** [https://multimodaal.netlify.app/](https://multimodaal.netlify.app/)

### Backend (Render)
- **Platform:** Render (Python web service)
- **Server:** `gunicorn` for WSGI production-ready deployment
- **Dependencies:** Installed via `requirements.txt`
- **Google Credentials:** Managed using Render Secret Files
- **System Requirements:** Render instance with minimum 2GB RAM; `ffmpeg` configured for audio processing
  


## System Flowchart

![System Flowchart](https://github.com/user-attachments/assets/c7857caa-2bdf-4cf8-b29b-7ff18486f010)

### Flow Breakdown:
1. **User Input:** User interacts via text, image, or audio on the React frontend
2. **API Call:** Axios sends requests to the Flask backend
3. **Service Routing:**
    - For Image: BLIP model
    - For Text/Speech: Google Cloud APIs
4. **Response Handling:** JSON (text/captions), audio file (TTS)
5. **Display:** Dynamic rendering of results in the UI



## Core Features

- **Multilingual Translation:** Detects and translates input text across languages
- **Text-to-Speech (TTS):** Converts translated text into natural-sounding speech
- **Speech-to-Text (STT):** Transcribes audio files in multiple languages with optional translation
- **Image Captioning:** Generates rich, descriptive captions from user-uploaded images using the BLIP model



## Technology Stack

- **Frontend:** React.js, Axios, HTML5/CSS3
- **Backend:** Python 3.x, Flask, Flask-CORS, gunicorn
- **AI & ML:**
  - Google Cloud (Translate, TTS, STT)
  - Hugging Face Transformers (BLIP model)
  - PyTorch, pydub, Pillow
- **Hosting:**
  - Netlify (frontend)
  - Render (backend)



## Prerequisites

- **Python:** 3.8+
- **Node.js & npm:** Node.js v16+
- **ffmpeg & ffprobe:** Required for audio file preprocessing
- **Google Cloud Project:** With necessary APIs enabled:
  - Cloud Translation API
  - Cloud Text-to-Speech API
  - Cloud Speech-to-Text API
- **Service Account Key:** `.json` file for authenticated API access



## Running Locally

1. **Backend Setup:**
   ```bash
   cd backend
   python app.py
   ```
2. **Frontend Access:**
   Open browser at `http://127.0.0.1:5000` or configured frontend port


## Presentation Slides

View our presentation covering architecture, design rationale, challenges, and outcomes:

**[View Presentation Slides](./Cloud_Presentation.pdf)**



## Summary

This project exemplifies how cloud-native services and modern machine learning models can be orchestrated into a cohesive, scalable solution for real-world, multimodal applications. With accurate speech/text/image capabilities, real-time responsiveness, and seamless cloud deployment, it sets the foundation for innovative applications in cross-lingual communication, accessibility, and content automation.

