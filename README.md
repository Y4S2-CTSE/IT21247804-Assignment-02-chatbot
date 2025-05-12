# CTSE Lecture Notes Chatbot

## Overview
A Gemini AI-powered chatbot that helps students access and query CTSE (Current Trends in Software Engineering) lecture content. Built using LangChain and Gradio, this chatbot processes lecture materials in various formats (PPTX, PDF, TXT) and provides intelligent responses based on the content.

## Features
- 📚 Processes multiple document formats (PowerPoint, PDF, Text files)
- 🤖 Powered by Google's Gemini AI for natural language understanding
- 🔍 Vector-based search for accurate information retrieval
- 💾 Persistent storage of processed lecture content
- 🌐 Web-based interface using Gradio
- 📝 Source attribution for responses

## Prerequisites
- Python 3.9 or higher
- Google Cloud Account with Gemini API access
- 4GB RAM minimum
- Windows/Linux/Mac OS

## Local Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/IT21247804-Assignment-02-chatbot.git
cd IT21247804-Assignment-02-chatbot
```

### 2. Create Virtual Environment
```bash
python -m venv venv
# On Windows
.\venv\Scripts\activate
# On Linux/Mac
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory:
```env
GOOGLE_API_KEY=your-google-api-key-here
VECTOR_STORE_DIR=./vector_store
LECTURES_DIR=./lectures
MODEL_NAME=gemini-pro
TEMPERATURE=0.7
TOP_P=0.85
MAX_TOKENS=1024
EMBEDDING_MODEL=all-MiniLM-L6-v2
```

### 5. Prepare Lecture Materials
1. Create a `lectures` directory
2. Add your lecture materials (PPTX, PDF, TXT files)
```bash
mkdir lectures
# Copy your lecture files to the lectures directory
```

### 6. Run the Application
```bash
python app.py
```

## Hugging Face Space Deployment

### 1. Prepare for Deployment
1. Create a new Space on Hugging Face
2. Choose "Gradio" as the SDK
3. Set the Space settings:
   - Python 3.9+
   - CPU architecture

### 2. Configure Space Variables
Add these secrets in your Space's Settings:
- `GOOGLE_API_KEY`
- Other configuration variables as needed

### 3. Upload Files
Required files:
- `app.py`
- `requirements.txt`
- `README.md`
- Create `lectures` directory in the Space

### 4. Space Configuration
Update the Space's `README.md` with:
```yaml
title: IT21247804 Assignment 02 Chatbot
emoji: 😻
colorFrom: gray
colorTo: red
sdk: gradio
sdk_version: 4.0.0
app_file: app.py
pinned: false
license: mit
```

## View Already deployed Huggingface space by the author
```bash
https://huggingface.co/spaces/Baddewithana/IT21247804-Assignment-02-chatbot
```

## Project Structure
```
IT21247804-Assignment-02-chatbot/
├── app.py              # Main application file
├── requirements.txt    # Python dependencies
├── .env               # Environment variables
├── .gitignore         # Git ignore rules
├── README.md          # Project documentation
├── lectures/          # Lecture materials
└── vector_store/      # Processed vector embeddings
```

## Technical Details
- **Framework**: LangChain + Gradio
- **AI Model**: Google Gemini Pro
- **Embeddings**: HuggingFace all-MiniLM-L6-v2
- **Vector Store**: FAISS
- **UI**: Gradio Web Interface

## Troubleshooting
1. **ModuleNotFoundError**: Run `pip install -r requirements.txt`
2. **API Key Error**: Check `.env` file configuration
3. **No Lectures Found**: Ensure files are in the `lectures` directory
4. **Memory Issues**: Reduce chunk size in `process_text` function

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Author
- IT21247804 - Baddewithana P
- For Current Trends in Software Engineering (SE4010) Assignment 2

## Acknowledgments
- Google Gemini AI
- LangChain Framework
- Gradio Team