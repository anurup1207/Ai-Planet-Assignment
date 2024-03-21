## AI Planet Chat App

AI Planet Chat App is a project designed to enable users to interact with a PDF document through a chat interface. The application utilizes React for the frontend and FastAPI for the backend. It consists of two main folders: Frontend and Backend. Both frontend and backend sections are intended to be run separately.

\#\# Getting Started

To get started with the AI Planet Chat App, follow these steps:

1. Clone the repository:

   \`\`\`bash
   git clone <repository_url>
   cd AI-Planet-Chat-App
   \`\`\`

2. Set up environment variables:

   Create a \`.env\` file in both the frontend and backend directories and add the following keys:


   \# Backend .env file
   OPENAI_API_KEY=
   DB_NAME=
   DB_USER=
   DB_PSWD=
   DB_HOST=
   DB_PORT=
   \`\`\`

   Replace \`<repository_url>\` with the actual URL of the repository.

3. Install dependencies:

   Navigate to the frontend and backend directories and install the dependencies:

   \`\`\`bash
   cd Frontend
   npm install
   cd ../Backend
   pip install -r requirements.txt
   \`\`\`

4. Run the backend server:

   \`\`\`bash
   uvicorn main:app --reload
   \`\`\`

5. Run the frontend server:

   \`\`\`bash
   npm start
   \`\`\`

6. Access the application:

   Visit \`http://localhost:3000\` in your web browser to access the AI Planet Chat App.

\#\# Architecture

The architecture of the AI Planet Chat App involves the following components:

![AI Planet Chat App](./images/LangChain.jpg)

- **Frontend**: The frontend is built using React and facilitates user interaction with the application. It handles uploading PDF files, sending questions, and displaying responses.

- **Backend**: The backend is developed using FastAPI and serves as the server-side component of the application. It receives PDF files, extracts text from them, processes user questions, generates responses based on the content of the PDF and user queries, and stores relevant data in a PostgreSQL database.

- **Text**: Chunking: The extracted text is divided into smaller chunks that can be processed effectively.

- **Language Model**: The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

- **Similarity Matching**: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

- **Response Generation**: The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.
- **Database**: The application uses a PostgreSQL database to store information such as the text and name of uploaded PDFs, along with timestamps.

- **Speech-to-Text**: An additional feature of the application is speech-to-text functionality, which allows users to speak instead of typing their queries. This feature enhances user accessibility and ease of use.

\#\# Usage

1. Upload a PDF document: Users can upload a PDF document through the frontend interface.

2. Ask questions: Once the PDF is uploaded, users can ask questions related to the content of the document using the chat interface.

3. Receive responses: The application generates responses based on the content of the PDF and user queries, providing relevant information to the user.

4. Speech-to-text: Users can utilize the speech-to-text feature to input their queries by speaking instead of typing.

\#\# Contributing

Contributions to the AI Planet Chat App are welcome. If you have any suggestions, feature requests, or bug reports, please feel free to submit them through the repository's issue tracker.

\#\# License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

\#\# Acknowledgments

Special thanks to OpenAI for providing the language model and embedding API used in this project.
