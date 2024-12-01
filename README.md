# Assistant-RAG-Multi-Mod-les
💬 Multi-Model RAG Assistant
This repository contains a Streamlit-based web application that serves as a Retrieval-Augmented Generation (RAG) assistant, allowing you to interact with multiple LLM models while leveraging relevant documents for accurate responses.

The assistant supports dynamic model selection, multi-document uploads (PDF, TXT, DOCX), and retrieval-based conversational memory for contextual interactions.

Features
🔍 Retrieve Relevant Documents: Processes and indexes uploaded documents for question answering.
🧠 Conversation Memory: Keeps track of conversation history for a coherent dialogue.
⚙ Multi-Model Support: Switch between various LLMs like Llama3.1, Mistral, Gemma, and others.
📂 Document Formats Supported: PDF, TXT, DOCX.
🎯 Adjustable Relevance Threshold: Customize how strictly the assistant matches your query to document content.
📥 Installation
Prerequisites
Ensure you have the following installed:

Python 3.8+
pip (Python package manager)
Steps
Clone this repository:

bash
Copy code
git clone https://github.com/your-username/multi-model-rag-assistant.git  
cd multi-model-rag-assistant  
Create and activate a virtual environment:

bash
Copy code
python -m venv venv  
source venv/bin/activate  # On Windows: venv\Scripts\activate  
Install dependencies:

bash
Copy code
pip install -r requirements.txt  
Install and start a local ChromaDB instance (for vector storage):

bash
Copy code
pip install chromadb  
chromadb --start  
Install and configure Ollama locally (to support OllamaLLM):

Follow the setup instructions at Ollama.
🚀 Usage
Start the Streamlit application:

bash
Copy code
streamlit run app.py  
Open your browser and navigate to the URL shown in your terminal (default: http://localhost:8501).

Upload Documents: Use the sidebar to upload supported document formats (PDF, TXT, DOCX).

Interact with the Assistant:

Select your preferred model (e.g., Llama3.1, Mistral).
Set the relevance threshold.
Enter your query in the input box to get context-aware responses.
🛠 Project Structure
graphql
Copy code
multi-model-rag-assistant/  
│  
├── app.py                  # Main Streamlit application  
├── requirements.txt        # Dependencies  
├── rag_database/           # Directory for ChromaDB persistent storage  
└── README.md               # Project documentation  
⚙ Configuration
Model Selection: Use the sidebar dropdown to switch between supported models.
Relevance Threshold: Customize the threshold for document relevance (default: 0.3).
Conversation History: Automatically stored in session state for coherent follow-ups.
🔧 Development
Add New Models
Add the model name to the model_name dropdown in app.py.
Ensure the model is properly configured with OllamaLLM or similar APIs.
Customize Document Loaders
Modify or extend the load_document function to support additional file formats.
🤝 Contributions
Contributions are welcome! Feel free to open an issue or submit a pull request.

📄 License
This project is licensed under the MIT License.
