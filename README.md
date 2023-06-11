# Flask API

This is a simple Flask API with two endpoints. The first endpoint accepts a JSON object containing a list of numbers and returns the sum of the numbers. The second endpoint accepts a JSON object containing two strings and returns the concatenated result. It also demonstrates error handling for invalid input.

## Requirements

- Python 3.x
- Flask

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/OmarEhab177/flask-sum-api.git
   cd flask-api
   ```

2. Create and activate a virtual environment (optional but recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Start the Flask server:

   ```bash
   python app.py
   ```

2. Once the server is running, you can send HTTP requests to the following endpoints:

   - **Sum Endpoint**
     
     - URL: `http://localhost:5000/sum`
     - Method: POST
     - Request Body:
       ```json
       {
         "numbers": [1, 2, 3, 4, 5]
       }
       ```
     - Response:
       ```json
       {
         "result": 15
       }
       ```

   - **Concatenate Endpoint**
     
     - URL: `http://localhost:5000/concatenate`
     - Method: POST
     - Request Body:
       ```json
       {
         "string1": "Hello",
         "string2": "World"
       }
       ```
     - Response:
       ```json
       {
         "result": "HelloWorld"
       }
       ```

3. If the request contains invalid input, such as missing keys or incorrect value types, the API will respond with an error message and a 400 Bad Request status code.
