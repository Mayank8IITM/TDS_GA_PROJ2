# TDS GA Solver

## Project Overview
TDS GA Solver is an LLM-based API designed to answer questions from the graded assignments of IIT Madras' Online Degree in Data Science. The API takes a question and optional file attachments as input and returns the correct answer.

## Features
- Accepts a question from any of the 5 graded assignments.
- Supports optional file attachments.
- Returns a JSON response containing the answer.
- Deployed on Vercel for easy access.

## API Endpoint
The API is hosted at:
```
https://your-app.vercel.app/
```

### Request Format
Send a `POST` request to the API with the question as form-data:
```sh
curl -X POST "https://your-app.vercel.app/" \
  -H "Content-Type: multipart/form-data" \
  -F "question=Download and unzip file abcd.zip which has a single extract.csv file inside. What is the value in the 'answer' column of the CSV file?" \
  -F "file=@abcd.zip"
```

### Response Format
The API will return a JSON object:
```json
{
  "answer": "1234567890"
}
```

## Installation & Setup
### Step 1: Clone the Repository
```sh
git clone https://github.com/user-name/repository-name.git
cd repository-name
```

### Step 2: Create a Virtual Environment
```sh
python3 -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate  # On Windows
```

### Step 3: Install Dependencies
```sh
pip install -r requirements.txt
pip freeze > requirements.txt
```

### Step 4: Run the API Locally
```sh
uvicorn main:app --reload
```

The API will be available at:
```
http://127.0.0.1:8000/
```

