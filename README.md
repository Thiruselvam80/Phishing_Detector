# Phishing Detector Web Application

A modern, modular web application for detecting phishing threats in URLs and emails, built with Python and Flask. The app combines rule-based heuristics, optional machine learning, and third-party threat intelligence APIs to provide accurate, real-time phishing detection. Designed for both technical and non-technical users, it features a user-friendly web interface, persistent scan history, and robust security features.

---

## Features
- **Modular Codebase:** Clean separation of logic for validation, detection, API integration, storage, and UI.
- **Phishing Detection Engine:** Combines rule-based, ML, and API-based detection for URLs and emails.
- **Admin Dashboard:** Review scan history, statistics, and detailed results.
- **User-Friendly Web UI:** Responsive, Bootstrap-powered interface with AJAX for real-time feedback.
- **Security:** Input sanitization, rate limiting, API key protection, and session management.
- **Persistent Storage:** All scans are saved in a SQLite database for audit and review.
- **Configurable:** API keys and settings via config file and environment variables.
- **Comprehensive Logging:** Tracks scan activity and errors for debugging and auditing.
- **Cross-Platform:** Runs on Windows, macOS, and Linux.
- **Deployable:** Ready for PythonAnywhere or any standard Python hosting.

---

## Technologies Used
| Technology   | Purpose                                                      |
|--------------|--------------------------------------------------------------|
| Python       | Core backend logic, detection engine, and utilities          |
| Flask        | Web framework for the interactive UI                         |
| SQLite       | Database for scan records                                    |
| requests     | HTTP requests to APIs and web content                        |
| markupsafe   | Input sanitization                                           |
| Bootstrap    | Responsive web design                                        |
| JavaScript   | AJAX and dynamic frontend                                    |
| HTML/CSS     | UI structure and styling                                     |
| Git & GitHub | Version control and publishing                               |
| (Optional) Machine Learning | Advanced phishing detection (ml_predictor.py) |

---

## Project Structure
```
phishing-detector/
├── app.py                      # Main Flask application
├── ml_predictor.py             # (Optional) ML model integration
├── requirements.txt            # Python dependencies
├── config.json                 # Configuration file
├── phishing_detector.db        # SQLite database
├── templates/                  # HTML templates
│   ├── index.html
│   ├── result.html
│   ├── admin_scans.html
│   ├── scan_detail.html
│   └── admin_login.html
├── static/                     # CSS, JS, assets
│   ├── style.css
│   └── script.js
├── pythonanywhere_wsgi.py      # WSGI entrypoint for deployment
├── README.md                   # Documentation
├── LICENSE                     # License info
├── demo.mp4                    # (Optional) Demo video
├── sample_report.pdf           # (Optional) Sample report
├── logs/                       # Log files
│   └── phishing_detector.log
```

---

## Setup & Usage

### 1. Clone the Repository
```
git clone https://github.com/yourusername/phishing-detector.git
cd phishing-detector
```

### 2. Create Virtual Environment & Install Dependencies
```
python -m venv venv
venv\Scripts\activate  # On Windows
# or
source venv/bin/activate  # On macOS/Linux
pip install -r requirements.txt
```

### 3. Set Environment Variables
Set your API keys and secret settings (example for Windows):
```
set VIRUSTOTAL_API_KEY=your_virustotal_key
set PHISHTANK_API_KEY=your_phishtank_key
set FLASK_SECRET_KEY=your_secret_key
```

### 4. Run the Application
```
python app.py
```
Visit [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

---

## Deployment (PythonAnywhere)
1. Zip your project (excluding venv, __pycache__, and large files).
2. Upload and extract on PythonAnywhere.
3. Set up a new web app and configure the WSGI file to point to `app.py`.
4. Install dependencies: `pip install -r requirements.txt`.
5. Set environment variables in the PythonAnywhere dashboard.
6. Reload the web app and test online.

---

## License
This project is open-source and available under the MIT License.

---

## Acknowledgements
- VirusTotal and PhishTank for threat intelligence APIs
- Flask, Bootstrap, and the open-source community

---

## Contact
For questions or contributions, open an issue or contact the maintainer via GitHub.
