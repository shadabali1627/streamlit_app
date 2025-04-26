SimpleQA Chatbot
A Streamlit-based chatbot that answers user queries using a combination of a pre-loaded SimpleQA dataset and the Gemini API with Retrieval-Augmented Generation (RAG). The app employs fuzzy matching to find relevant answers in the dataset and falls back to the Gemini API for unmatched queries.
Features

Dataset-Driven Answers: Uses the basicv8vc/SimpleQA dataset from Hugging Face for quick, accurate responses.
Fuzzy Matching: Matches user queries to dataset questions with a configurable similarity threshold.
Gemini API Integration: Provides intelligent answers using the Gemini 1.5 Pro model when dataset answers are unavailable.
Chat History: Displays previous interactions in a sidebar for easy reference.
Streamlit Interface: Simple, user-friendly web interface for query input and response display.

Prerequisites

Python 3.8 or higher
A valid Gemini API key from Google
GitHub account for deployment to Streamlit Cloud
Internet access for loading the SimpleQA dataset

Setup Instructions
Local Setup

Clone the Repository:
git clone https://github.com/your-username/simpleqa-chatbot.git
cd simpleqa-chatbot


Create a Virtual Environment (optional but recommended):
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install Dependencies:
pip install -r requirements.txt


Set Up Environment Variables:

Create a .env file in the project root.
Add your Gemini API key:GEMINI_API_KEY=your-gemini-api-key-here




Run the App Locally:
streamlit run app.py


Open the provided URL (e.g., http://localhost:8501) in your browser.



Dependencies
Listed in requirements.txt:

streamlit
python-dotenv
pandas
fuzzywuzzy
datasets
google-generativeai
python-Levenshtein (optional, for faster fuzzy matching)

Deployment to Streamlit Cloud

Push to GitHub:

Create a GitHub repository and push your project files.
Exclude .env by adding it to .gitignore:.env




Deploy on Streamlit Cloud:

Log in to Streamlit Community Cloud with your GitHub account.
Create a new app, select your repository, and specify app.py as the main file.
In the app's "Settings" > "Secrets," add:GEMINI_API_KEY = "your-gemini-api-key-here"


Click "Deploy" to launch the app.


Verify:

Access the app via the provided Streamlit Cloud URL.
Check logs in the Streamlit Cloud dashboard for debugging.



Usage

Enter a Query: Type your question in the text input field.
View Response: The app returns an answer from the SimpleQA dataset or the Gemini API.
Check Source: Responses indicate whether they come from the dataset or the Gemini API.
Review History: Past interactions are shown in the sidebar.

Troubleshooting

API Key Error: Ensure GEMINI_API_KEY is set correctly in Streamlit Cloud secrets or your local .env file.
Dataset Loading Failure: Verify internet connectivity and the availability of the basicv8vc/SimpleQA dataset on Hugging Face.
Slow Performance: Install python-Levenshtein for faster fuzzy matching or adjust the similarity threshold in app.py.

Contributing
Contributions are welcome! Please:

Fork the repository.
Create a feature branch (git checkout -b feature-name).
Commit changes (git commit -m "Add feature").
Push to the branch (git push origin feature-name).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Built with Streamlit and Google Gemini API.
Uses the SimpleQA dataset by basicv8vc.

# streamlit_app
