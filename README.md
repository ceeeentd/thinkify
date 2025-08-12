# Thinkify

Thinkify is a vibrant space where people from diverse backgrounds and interests come together to engage in meaningful conversations, fostering an environment rich in idea exchange, knowledge sharing, and diverse experiences.

# Preview

<img src="/preview.png">
<a href="https://thinkify.vercel.app" target="_blank">Live Preview</a> | <a href="https://thinkify-server.vercel.app" target="_blank">Live API</a> | <a href="https://documenter.getpostman.com/view/27027258/2sA3dxEXJh" target="_blank">Postman</a>

# Requirements

[Install Node On Your Device](https://nodejs.org/)

# How to Run

```
git clone https://github.com/masum184e/thinkify.git

# BACKEND
cd server
npm install
npx nodemon index.js

# FRONTEND
cd ../client
npm install
npm run dev
```

# Environment Variables

## Frontend

```
VITE_SERVER_ENDPOINT = https://thinkify-server.vercel.app:3000/api
VITE_TOKEN_KEY = thinkify
VITE_USER_ROLE = role
VITE_COOKIE_EXPIRES = 1
```

## Backend

```
PORT = 3000
DATABASE_URL = mongodb://localhost:27017/
DATABASE_NAME = thinkify
BCRYPT_GEN_SALT_NUMBER = 10
JWT_SECRET_KEY = abcdefghijklmnopqrstuvwxyz
COOKIE_EXPIRES = 5d
COOKIE_KEY = thinkify
UPLOAD_DIRECTORY = uploads
```

## CI/CD Steps/Explanation

This project uses **GitHub Actions** to automate the build and deployment process.  
The workflow runs automatically whenever code is pushed to the `main` branch.

### How It Works

1. **Trigger**
   - The workflow is triggered on every push to the `main` branch.

2. **Runs on**
   - Executes in a fresh **Ubuntu** virtual machine (`ubuntu-latest`).

3. **Steps**
   - **Checkout repository**  
     Uses `actions/checkout@v3` to pull the latest version of the code.
   - **Setup Node.js**  
     Installs **Node.js v18** 
   - **Install backend dependencies**  
     CD to the `server` folder and installs required packages with `npm install`.
   - **Install frontend dependencies**  
     CD to the `client` folder and installs required packages with `npm install`.
   - **Mock Deployment**  
     Simulates a deployment by printing `Deploying Thinkify...` to the console.



