# Portfolio Shortlisting and Email Generation

## Overview 

This Streamlit application automates the shortlisting of portfolios based on user queries and generates emails to recruitment teams. It leverages the power of **LangChain** and **LLM models** for natural language understanding and generative AI capabilities.

---


## **Table of Contents**

- [Overview ](#Overview)
- [Features](#features)
- [Prerequisites](#Prerequisites)
- [Setup and Installation](#setup-and-installation)
- [File Structure](#File Structure
- [Technologies Used](#technologies-used)
- [Usage](#usage)
- [Result](#Result)
---

## Features

- **Multi-format Portfolio Uploads**: Supports CSV, Excel, PDF, and plain text files.
- **Query Portfolios**: Users can ask specific questions about uploaded portfolios.
- **Vector-Based Search**: Efficient search and retrieval using embeddings.
- **Automated Email Generation**: Generates professional emails to recruiters based on shortlisted portfolios.

---

## Prerequisites

Ensure the following tools and libraries are installed:

- **Python 3.8+**
- **Streamlit**: For building and running the application.
- **LangChain**: For LLM-based workflows.
- **FAISS**: For vector-based document retrieval.
- **Google Generative AI Embeddings**: For embedding creation.
- **PyPDFLoader**: For parsing PDF documents.
- **dotenv**: For managing API keys and environment variables.

---

## Setup Instructions

1. **Clone the Repository**  
   ```bash
   git clone 
   cd portfolio-shortlisting
   ```

2. **Install Dependencies**  
   Create a virtual environment and install required Python libraries.  
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # For Linux/macOS
   venv\Scripts\activate     # For Windows

   pip install -r requirements.txt
   ```

3. **Set Environment Variables**  
   Create a `.env` file in the root directory and add the required API keys:
   ```env
   GROQ_API_KEY=your_groq_api_key
   GOOGLE_API_KEY=your_google_api_key
   ```

4. **Run the Application**  
   Start the Streamlit app:  
   ```bash
   streamlit run app.py
   ```
---


## File Structure

```
portfolio-shortlisting/
│
├── app.py                # Main application file
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables (ignored in version control)
├── README.md             # Documentation file
└── sample-data/          # Sample files for testing
    ├── portfolios.csv
    ├── portfolios.xlsx
    ├── portfolios.pdf
    └── portfolios.txt
```
---

## Technologies Used

The required dependencies are listed in `requirements.txt`. Key libraries include:

- `streamlit`
- `langchain`
- `faiss-cpu`
- `langchain-community`
- `langchain-google-genai`
- `pandas`
- `dotenv`

Install them using:
```bash
pip install -r requirements.txt
```

---

## Usage

1. **Upload Portfolio Files**  
   Upload one or more portfolio files in the supported formats (CSV, Excel, PDF, or plain text).

2. **Create Vector Store**  
   Click the **"Create Vector Store"** button to process the uploaded files.

3. **Ask Questions**  
   Enter a query related to the portfolios in the input box.

4. **View Results**  
   - The application will display the retrieved answers.
   - It also generates an email to recruiters with details of shortlisted candidates.

---

## Supported File Formats

- **CSV**: Each row should contain portfolio details like name, skills, experience, and location.
- **Excel**: Similar structure as CSV.
- **PDF**: The application parses text content for processing.
- **Text**: Plain text documents.

---



