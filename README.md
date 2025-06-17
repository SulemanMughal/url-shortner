# URL Shortener

A Django-based web application that allows users to shorten long URLs into shorter, easy-to-share links. This project demonstrates model design, form handling, and basic analytics for tracking URL usage.

## Features

- **URL shortening:** Converts long URLs into concise, unique short links.
- **Redirection:** Redirects users from short links to the original URLs.
- **Tracking analytics:** Records how many times a short URL has been visited.
- **Admin interface:** Manage and view shortened URLs via Django admin.
- **Form validation:** User-friendly Django forms for URL input.
- **Random code generation:** Ensures unique short links for each URL.

## Demo

![Data Output](https://github.com/SulemanMughal/url-shortner/blob/main/demo/demo.png)

## Quick Start

### Prerequisites

- Python 3.6+
- Django 3.x

### Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/SulemanMughal/url-shortner.git
    cd url-shortner/url_shortner
    ```

2. **Install dependencies**
    ```bash
    pip install django
    ```

3. **Apply migrations**
    ```bash
    python manage.py migrate
    ```

4. **Run the server**
    ```bash
    python manage.py runserver
    ```

5. **Open in browser**
    - Visit `http://127.0.0.1:8000/` to access the URL shortener.

## Usage

1. Enter a long URL in the form and submit.
2. Receive a shortened URL to share.
3. When the short URL is visited, users are redirected to the original link.
4. The number of times each short URL is followed is tracked.

## Project Structure

```
url_shortner/
├── manage.py
├── url_shortner/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
├── urlshortener/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── migrations/
│   ├── models.py
│   ├── templates/
│   ├── tests.py
│   ├── urls.py
│   ├── utils.py
│   └── views.py
```

## Main Components

- **Model (`Shortener`):** Stores original and short URLs, creation date, and visit count.
- **Views:** 
  - `home_view` — handles the form for submitting long URLs and displaying the result.
  - `redirect_url_view` — handles redirection from short to long URLs and increments visit count.
- **Forms:** Django forms for URL input and validation.
- **Utilities:** Random code generator for creating unique short URLs.
- **Templates:** Responsive HTML (Bootstrap) for UI.

## Django Admin

- Run `python manage.py createsuperuser` to create an admin account.
- Visit `/admin` to manage short URLs.

## Configuration

- By default, uses SQLite for storage.
- Adjust settings in `url_shortner/settings.py` as needed.

## License

MIT License

## Author

[Suleman Mughal](https://github.com/SulemanMughal)
