# JsonApi

## Description
This is a Next.js API that takes in unstructured input, such as an HTML string, and returns a structured JSON output. It extracts various elements from the HTML, including the title, meta data, and any other elements specified by the user.

## Installation
1. Clone the repository: `git clone https://github.com/yourusername/JsonApi.git`
2. Navigate to the project directory: `cd JsonApi`
3. Install the dependencies: `npm install`

## Usage
Send a POST request to the `/api/extract` endpoint with the HTML string in the request body. The API will return a JSON object with the extracted data.

## Example
```javascript
fetch('http://localhost:3000/api/extract', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    html: '<!DOCTYPE html><html><head><title>Test Page</title></head><body><h1>Welcome to the Test Page</h1></body></html>',
  }),
})
.then(response => response.json())
.then(data => console.log(data));
