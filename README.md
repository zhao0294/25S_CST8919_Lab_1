# CST8919 Lab 1: Implementing User Login with Flask and Auth0


## Objective

In this lab, you will build a Python web application using Flask and integrate it with **Auth0** for secure authentication.

You will follow the official Auth0 Quickstart guide:
🔗 [Auth0 Python Web App Quickstart](https://auth0.com/docs/quickstart/webapp/python#configure-auth0)

By the end of this assignment, you should have a Flask app that supports login and logout via Auth0, with additional customization.

---
## About Auth0, Identity Provider & Service Provider

### What is Auth0?

**Auth0** is an **authentication and authorization platform** that helps developers add secure login, logout, and identity management features to applications with minimal effort. Instead of building user authentication from scratch, you can use Auth0 to handle login flows, tokens, and user profiles securely.

### Identity Provider (IdP)

An **Identity Provider (IdP)** is the system that verifies user identities. Examples include:
- Auth0
- Google
- Facebook
- Microsoft Entra ID

The IdP is responsible for:
- Handling login screens
- Verifying credentials
- Returning identity information to the app (like name, email, etc.)

### Service Provider (SP) / Relying Party (RP)

A **Service Provider (SP)** or **Relying Party (RP)** is the application or service that the user is trying to access — in this case, **your Flask web app**.

The SP:
- Redirects users to the IdP (Auth0) for login
- Receives authentication tokens from the IdP
- Grants or denies access based on login status

In this lab, **your Flask app is the Service Provider** and **Auth0 acts as the Identity Provider / Relying Party (RP)**.

---

## Tasks

### 1. Follow the Tutorial

- Complete the steps from **"Configure Auth0"** to the end of the Auth0 Quickstart tutorial.
- Ensure the app runs locally and that users can successfully log in and log out.

### 2. Customize the App

Make the following additions to the base tutorial:

- Add a new route `/protected` for a **"Protected Page"** that only authenticated users can access.
- If a user tries to access `/protected` while not logged in, redirect them to the login page.

### 3. Documentation

Include a `README.md` with:

- Instructions for setting up the app, including how to configure Auth0.
- Commands to install dependencies and run the app locally.
- Example `.env` file or instructions for setting environment variables.
- **A link to a 5-minute YouTube video demo** showing:
  - How your app works (login, protected page)
  - A brief explanation of your code and what you learned

### 4. GitHub Repository

- Initialize a Git repository for your project.
- Make **frequent commits** with meaningful commit messages.
- Push your code to a **public GitHub repository**.
- Include the **YouTube demo link in the README.md**.

---

## Submission Instructions

Submit your **GitHub repository link** via Brightspace.

**Deadline**: Wednesday, 28 May 2025

---

## Tips

- Test your app before submitting — especially login, logout, and protected routes.
- Practice your demo before recording to stay within the 5-minute limit.
- Refer to the Auth0 documentation or ask for help if you get stuck.


