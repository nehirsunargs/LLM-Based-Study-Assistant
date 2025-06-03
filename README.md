# AI-Powered Concept Explainer 

AI Study Buddy is a web application that allows users to get explanations for various concepts using an AI-powered backend. The app lets you input a concept, and it will provide an explanation powered by the Mistral-7B-Instruct model.

## Features

- Input a concept and get a detailed explanation.
- Easy-to-use UI built with React.
- Backend built using Flask and powered by the Mistral model API.
- CORS-enabled for local development.

## Tech Stack

- **Frontend**: React
- **Backend**: Flask
- **AI Model**: Mistral-7B-Instruct via the Together API
- **Environment Management**: Python `.env` for API keys
- **CORS**: Flask-CORS to handle cross-origin requests

## Getting Started

### Prerequisites

1. **Frontend (React)**:
   - Node.js (v14 or higher) installed on your machine.
   - `npm` or `yarn` for managing dependencies.

2. **Backend (Flask)**:
   - Python 3.7 or higher.
   - `pip` for installing dependencies.
   - `.env` file for storing your API key.

### Installation

#### 1. Clone the repository

```bash
git clone https://github.com/nehirsunargs/ai-study-buddy.git
cd ai-study-buddy
```

#### 2. Install Backend Dependencies

- Navigate to the backend folder.
  
```bash
cd backend
```

- Create a virtual environment and install dependencies:

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
pip install -r requirements.txt
```

#### 3. Set up `.env`

In the backend folder, create a `.env` file and add your **API Key** from Together API:

```
API_KEY=your_api_key_here
```

#### 4. Run the Backend

Start the Flask server:

```bash
python app.py
```

The backend should now be running on `http://127.0.0.1:8000`.

#### 5. Install Frontend Dependencies

- Navigate to the frontend folder.

```bash
cd frontend
```

- Install the required npm dependencies:

```bash
npm install
```

#### 6. Run the Frontend

Start the React app:

```bash
npm start
```

The frontend should now be accessible at `http://localhost:3000`.

### Usage

1. Open the frontend application in your browser.
2. Enter a concept in the input field (e.g., "Quantum Physics").
3. Press the "Explain" button to receive an AI-generated explanation of the concept.
4. If an error occurs, it will display an error message on the screen.

### Example

Here’s an example of a successful request and response:

**Request:**
```json
{
  "concept": "Quantum Physics"
}
```

**Response:**
```json
{
  "explanation": "Quantum physics is the branch of physics that deals with the behavior of matter and energy at very small scales, such as atoms and subatomic particles..."
}
```

### Error Handling

If no explanation is found or an error occurs, the frontend will display a message like:
- "No explanation found."
- "There was an error processing your request."

### Troubleshooting

- **Backend not responding**: Ensure that the Flask app is running on the correct port (`8000`) and that you've set up the `.env` file correctly with your API key.
- **CORS issues**: If you encounter CORS issues, ensure that `flask-cors` is correctly installed and configured.

### Author
This project was created by Nehir Sunar
