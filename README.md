# ASD Whistleblowing App

The **ASD Whistleblowing App** is a secure and user-friendly web application designed for healthcare professionals to anonymously report unethical or misconduct practices within their organization. Built using Django, the application ensures confidentiality, enables effective report management, and provides an easy-to-use interface for users and administrators.

## Table of Contents
1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Installation and Setup](#installation-and-setup)
4. [Usage](#usage)
5. [File Structure](#file-structure)
6. [Future Improvements](#future-improvements)
7. [License](#license)

---

## Features
- **Anonymous Reporting**: Submit reports without revealing your identity.
- **User Roles**:
  - **Admin**: Manage reports, update their statuses, and provide resolution feedback.
  - **Regular Users**: Submit new reports and track their progress.
- **File Uploads**: Attach supporting evidence to reports.
- **Dashboards**:
  - **Admin Dashboard**: View all reports categorized by status (New, In Progress, Resolved).
  - **User Dashboard**: Track the status of personal reports for logged-in users.
- **Authentication**:
  - Secure user authentication using Django Allauth.
  - Social login capabilities.

---

## Technologies Used
- **Backend**: Django (Python)
- **Database**: PostgreSQL
- **Deployment**: Gunicorn, AWS (with Boto3)
- **Frontend**: HTML, CSS, Bootstrap
- **Other Tools**:
  - Django Allauth for user authentication.
  - File handling with Django models and AWS integration.

---

## Installation and Setup

### Prerequisites
- Python 3.8+
- PostgreSQL
- AWS S3 bucket (for file uploads)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/AkanMNdem/asd-whistleblowing-app.git
   cd asd-whistleblowing-app
   ```
2. Create and activate a virtual environment:
   ```bash
    python3 -m venv venv
    source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
    pip install -r requirements.txt
   ```
4. Create a PostgreSQL database and update the DATABASES section in mysite/settings.py:
   ```python
    DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '5432',
      }
    }
   ```
5. Run database migrations:
   ```bash
    python manage.py migrate
   ```
6. Update the AWS credentials in settings.py:
   ```python
    AWS_ACCESS_KEY_ID = 'your_access_key'
    AWS_SECRET_ACCESS_KEY = 'your_secret_key'
    AWS_STORAGE_BUCKET_NAME = 'your_bucket_name'
   ```
7. l
   ```bash
    python manage.py runserver
   ```
8. Access the app:
   Visit http://127.0.0.1:8000/ in your browser.
