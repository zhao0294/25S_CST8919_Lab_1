# CST8919 Lab 1: Implementing User Login with Flask and Auth0

This is a simple Flask web application that implements secure user authentication using Auth0. It supports login, logout, and a protected route that is accessible only to authenticated users.

## Features

- Auth0-based login and logout
- Protected route (/protected) accessible only to logged-in users
- Session-based user display on the homepage
- Tested locally on macOS (M4)

## Project Structure

<pre>

flask-auth0-app/
├── server.py
├── .env
├── requirements.txt
└── templates/
    ├── home.html
    └── protected.html
</pre>

## How to Run Locally

1. Clone this repository (or fork and clone if from course repo)

```bash

git clone https://github.com/ramymohamed10/25S_CST8919_Lab_1
cd 25S_CST8919_Lab_1/flask-auth0-app

```

2. Create and activate a Python virtual environment

```bash

python3 -m venv venv
source venv/bin/activate

```

3. Create requirements.txt

```bash

echo "flask>=2.0.3
python-dotenv>=0.19.2
authlib>=1.0
requests>=2.27.1" > requirements.txt

```

4. Install dependencies

```bash

pip install -r requirements.txt

```

5. Go to Auth0 Dashboard and create a new "Regular Web Application"
  * Allowed Callback URLs: http://localhost:3000/callback
  * Allowed Logout URLs: http://localhost:3000
  * After creation, copy:
    * Client ID
    * Client Secret
    * Domain (e.g. your-tenant.auth0.com)

6. Create a `.env` file in the root folder:

```bash

touch .env
open .env

```

fill it with:

```env

AUTH0_CLIENT_ID=your_auth0_client_id
AUTH0_CLIENT_SECRET=your_auth0_client_secret
AUTH0_DOMAIN=your-tenant.auth0.com
APP_SECRET_KEY=your_generated_app_secret_key
PORT=3000

```

Generate a secret key with:

```bash

openssl rand -hex 32

```

> ⚠️ Note: Never upload your `.env` file to GitHub. It contains secrets!

7. Run the app

```bash
python server.py
```

Then visit http://localhost:3000 in your browser.

## Demo Pages

- `/` – Homepage showing login/logout links
- `/login` – Starts Auth0 login flow
- `/callback` – Handles Auth0 redirect after login
- `/logout` – Logs out and clears session
- `/protected` – Requires login, otherwise redirects to login

## Demo Video

[Watch on YouTube](https://youtube.com/your-demo-link)

This video shows:

- Logging in and out using Auth0
- Visiting the protected page
- Brief explanation of how the app works

## What I Learned

- How to integrate Auth0 into a Flask app using Authlib
- How to manage user sessions with Flask
- How to protect specific routes from unauthorized access
- How to create a clean and testable Flask web app

## Submission

- GitHub repo: https://github.com/zhao0294/25S_CST8919_Lab_1
- Demo video: Linked above
- All features have been tested and verified