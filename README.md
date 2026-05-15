# NLP Assignment HRY: Agus Robot Document Chatbot

A Streamlit-based chatbot application that allows users to upload document files (PDF and DOCX) and interact with their content using Google's Generative AI (Gemini 1.5 Flash). The application extracts text from uploaded documents—utilizing Google Cloud Vision for robust PDF OCR—and uses that text as context to answer user queries in a conversational interface.

## 🌟 Features

* **Document Upload & Preview:** Supports both `.pdf` and `.docx` file formats with real-time text extraction and sidebar previews.
* **Intelligent Text Extraction:** * Uses `PyPDF2` and `google-cloud-vision` (OCR) to ensure text is accurately extracted from PDFs, even if they contain images.
  * Uses `python-docx` for parsing Word documents.
* **AI-Powered Chat:** Integrates with the `gemini-1.5-flash` model to answer context-specific questions based on the uploaded documents.
* **Adjustable Responses:** Users can toggle between Short, Medium, and Long response lengths.
* **Contextual Awareness:** The app validates user queries to ensure they are related to the uploaded document before sending requests to the API.
* **Export Chat History:** Download your conversation history as a `.txt` file for later reference.

## 📋 Prerequisites

Ensure you have Python 3.8+ installed. You will need the following Python libraries to run this project:

* `streamlit`
* `google-generativeai`
* `google-cloud-vision`
* `PyPDF2`
* `python-docx`
* `nltk`
* `fpdf`
* `python-dotenv` (For secure environment variable management)

## 🚀 Installation & Setup

**1. Clone the repository**
```bash
git clone [https://github.com/yourusername/nlp_assignment_hry.git](https://github.com/yourusername/nlp_assignment_hry.git)
cd nlp_assignment_hry
2. Install dependencies
It is recommended to use a virtual environment. Install the required packages using pip:

Bash
pip install -r requirements.txt
(Note: If you don't have a requirements.txt file, you can install them directly: pip install streamlit google-generativeai google-cloud-vision PyPDF2 python-docx nltk fpdf python-dotenv)

3. Configure API Keys securely
This project requires two sets of credentials. Never commit these files to GitHub. Ensure your .gitignore is set up properly.

Gemini API Key: Create a file named .env in the root directory and add your key:

Cuplikan kode
GEMINI_API_KEY="your_gemini_api_key_here"
Google Cloud Vision Service Account: Place your Google Cloud service account JSON key file in the root directory. Ensure the filename matches the one specified in app.py (e.g., chat-and-pdf-file-project-*.json), or update app.py to match your new key's filename.

💻 Usage
Run the application using Streamlit:

Bash
streamlit run app.py
Open the provided Local URL (usually http://localhost:8501) in your web browser.

Upload a .pdf or .docx file using the sidebar.

Review the extracted text in the sidebar preview.

Type your questions in the chat input box at the bottom of the screen.

📂 Project Structure
Plaintext
NLP_ASSIGNMENT_HRY/
│
├── app.py                  # Main Streamlit application script
├── .env                    # Environment variables (Gemini API Key) - DO NOT COMMIT
├── .gitignore              # Specifies intentionally untracked files to ignore
├── README.md               # Project documentation
└── [your-gcp-key].json     # Google Cloud Service Account key - DO N
