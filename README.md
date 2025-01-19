# Text Editor with AI Features (Backend)

Welcome to the backend repository for the AI-powered text editor! This repository provides the API and AI capabilities for the text editor, including document translation and chat with document content.

## Features

- **Flask**: Lightweight and efficient backend framework.
- **LangChain**: Framework for building AI-powered applications.
- **GROQ**: Querying AI for document insights and translation.
- **APIs**:
  - Chat with document: AI-powered interaction with document content.
  - Translate document: Translate text into multiple languages.
- **Deployed on Render**: Scalable backend hosting.

---

## Installation and Setup

### Prerequisites
- Python (v3.8+)
- Virtual Environment (optional but recommended)

### Steps
1. Clone this repository:
   ```bash
   git clone <backend-repo-url>
   cd <repository-name>
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the root directory with the following variables:
   ```env
   GROQ_API_KEY =<groq-api-key>
   ```

   > **Note**: To set up Firebase, you need to download the `service_key.json` file from your Firebase project. Extract its contents and save it as a file referenced by the `FIREBASE_CREDENTIALS` variable.

5. Run the Flask development server:
   ```bash
   flask run
   ```

6. The API will be available at [http://localhost:5000](http://localhost:5000).

---

## Deployment
The backend is deployed on Render. To deploy updates:
1. Push changes to the main branch.
2. Render will automatically build and deploy the latest changes.

---

## API Endpoints
### Base URL
Set the base URL in the frontend `.env.local` file to point to the backend:
```
NEXT_PUBLIC_BASE_URL=<backend-deployed-url>
```

### Example Endpoints
- **Chat with Document**:
  ```
  POST /api/chat
  Body: { "document": "<document-content>", "query": "<your-query>" }
  ```
- **Translate Document**:
  ```
  POST /api/translate
  Body: { "document": "<document-content>", "language": "<target-language>" }
  ```

---

## Connection to Frontend Repository
This repository is designed to work seamlessly with the frontend repository, which provides the user interface for the text editor.

### Frontend Repository
Find the frontend repository here: [Frontend Repository](https://github.com/Abhijeet314/Ai-TextEditor/tree/main)

Ensure that the frontend `.env.local` file points to this backend's deployed URL for proper integration.

---

## Technologies Used
- **Backend**: Flask
- **AI Features**: LangChain, Groq API
- **Deployment**: Render

---

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch.
3. Commit your changes and create a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

