# 🌐 ARX_Dev API Documentation

Welcome to the **ARX_Dev API Documentation**. This guide provides details on available API endpoints, request formats, and expected responses.

---

## 🔹 Base URL
All API requests are made to:

http://localhost:8000/api/

*(Replace `localhost` with your server IP or domain if deployed.)*
---

## 📌 Authentication
If authentication is required, include a token in the headers:
```sh
Authorization: Bearer YOUR_ACCESS_TOKEN

Example:

curl -H "Authorization: Bearer my_token" http://localhost:8000/api/status

## 🔹 Endpoints

### Get API Status
Check if the API is running.

GET /api/status

curl -X GET http://localhost:8000/api/status

Response
{
  "status": "running",
  "version": "1.0.0"
}

### Retrieve Data
Fetch stored records.

GET /api/data

curl -X GET http://localhost:8000/api/data

Response
[
  {
    "id": 1,
    "name": "Sample Data",
    "timestamp": "2024-03-02T12:00:00Z"
  }
]

### Submit Data
Send new data to the API.

POST /api/data

curl -X POST http://localhost:8000/api/data -H "Content-Type: application/json" -d '{"name": "New Entry"}'

Request Body
{
  "name": "New Entry"
}

Response
{
  "message": "Data added successfully",
  "id": 2
}

### Update an Entry
Modify an existing record.

PUT /api/data/{id}

curl -X PUT http://localhost:8000/api/data/1 -H "Content-Type: application/json" -d '{"name": "Updated Entry"}'

Request Body
{
  "name": "Updated Entry"
}

Response
{
  "message": "Data updated successfully"
}

### Delete an Entry
Remove a record.

DELETE /api/data/{id}

curl -X DELETE http://localhost:8000/api/data/1

Response
{
  "message": "Data deleted successfully"
}

## 📌 Error Handling
The API returns standard HTTP status codes:

Status Code                 Meaning
200 OK	                    Successful request
201 Created	                New resource created
400 Bad Request	            Invalid request parameters
401 Unauthorized	          Authentication failed
404 Not Found	              Requested resource not found
500 Internal Server Error	  Server encountered an issue

## 🛠️ Testing the API
Use Postman, cURL, or Python's requests library to test the API.

Example in Python:

import requests

response = requests.get("http://localhost:8000/api/status")
print(response.json())

## 🚀 Next Steps
See the Usage Guide for more details.
Learn how to contribute in Contributing.
