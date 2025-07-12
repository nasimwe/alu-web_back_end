# Flask i18n Project

This project demonstrates how to implement internationalization (i18n) and timezone localization in a Flask web application using Flask-Babel and pytz.

## 📚 Learning Objectives

- Parameterize Flask templates for multiple languages (English and French).
- Detect user locale from URL parameters, request headers, or user preferences.
- Localize and display current timestamps based on user-specific time zones.
- Simulate user login and preferences for locale and timezone handling.

## 🛠️ Technologies Used

- Python 3.7
- Flask
- Flask-Babel
- pytz

## ✅ Requirements

- Python files follow `pycodestyle` (v2.5)
- All Python files are executable and include:
  ```python
  #!/usr/bin/env python3
````

* All modules, classes, and functions are fully documented with meaningful docstrings.
* All functions and coroutines are type-annotated.

## 🚀 Features

### 0. Basic Flask App

A simple `/` route returning a localized homepage.

### 1. Basic Babel Setup

Initialized Babel with English and French as supported languages. Default locale is English and timezone is UTC.

### 2. Get Locale from Request

Detects the best match language from the `Accept-Language` HTTP header.

### 3. Parametrize Templates

Templates use message IDs (`home_title`, `home_header`) and translation dictionaries (`.po` and `.mo` files) for language-specific content.

### 4. Force Locale via URL

Allows users to force a locale using `?locale=en|fr`.

### 5. Mock Login

Simulates user login with `login_as` parameter and displays personalized greetings.

### 6. Use User Locale

Locale preference can be derived from the user profile, URL, or request headers, in that order of priority.

### 7. Infer Timezone

Handles user and URL-based time zone preferences. Falls back to UTC if invalid or unspecified.

### 8. Display Current Time

Renders the current time localized to the selected timezone, displayed in the proper locale format.

## 🧪 Usage

```bash
# Set environment variable
export FLASK_APP=app.py

# Run the Flask server
flask run
```

* Access: `http://127.0.0.1:5000/`
* Force French: `http://127.0.0.1:5000/?locale=fr`
* Simulate user login: `http://127.0.0.1:5000/?login_as=2`
* Set time zone: `http://127.0.0.1:5000/?timezone=US/Central`

## 📁 File Structure

```
├── app.py                 # Final Flask app
├── babel.cfg             # Babel extraction config
├── templates/
│   └── index.html        # Jinja2 template with i18n support
├── translations/
│   ├── en/LC_MESSAGES/messages.po/.mo
│   └── fr/LC_MESSAGES/messages.po/.mo
├── README.md
```

## 📜 License

This project is part of the ALU Web Backend Curriculum and is for educational purposes.

---