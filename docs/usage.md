# 📘 ARX_Dev Usage Guide

This guide explains how to use the **Artificial Reality Xchange (ARX)** system after installation.

---

## 🚀 Running the Application

### 🔹 1. Navigate to the Project Directory
Ensure you're inside the correct folder before running any commands:
```sh
cd /path/to/ARX_Dev

### 🔹 2. Activate the Virtual Environment (If Using Python)
For Python-based setups:
```sh
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows

#### 🛠️ Available Commands
#####🔹 Start the Application
Depending on your setup, run:

Python-based Application
```sh
python main.py

Node.js-based Application
```sh
npm start

#### 🖥️ Using the Web Interface
Open your web browser and go to:

http://localhost:8000

If it's a command-line tool, follow the on-screen prompts.

#### ⚙️ Configuration & Customization
You can customize the project by modifying config files in the /config folder.

Change default settings: Edit config/settings.json
Modify logging settings: Edit config/logging.conf

#### 📂 Data Management
If the project processes data, ensure:

Input data is stored in the /data folder.
Results are saved in /output or /logs.

📡 API Usage (If Applicable)
If ARX provides an API, you can make requests like:

sh

curl -X GET http://localhost:8000/api/status

or in Python:

import requests
response = requests.get("http://localhost:8000/api/status")
print(response.json())

#### 🤖 AI Features (If Applicable)
If the project includes AI-driven functionality:

Model Training: Run train.py
Inference: Run predict.py

#### ❓ Troubleshooting

App not starting? Run:
sh
python main.py --debug

Port in use? Check with:
sh
netstat -an | grep 8000  # Mac/Linux
netstat -ano | findstr :8000  # Windows

Permissions issue? Try:
sh
sudo python main.py

#### 🎯 Next Steps
Read the API Documentation for detailed API usage.
See FAQ for common questions.

