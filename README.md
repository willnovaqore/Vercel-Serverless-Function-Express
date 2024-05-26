# Vercel Serverless Function Template

This repository contains a simple Vercel serverless function template for 2024. It is designed to be a starting point for deploying serverless functions on Vercel.

## Getting Started

### Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/techdevwill/Vercel-Serverless-Function-Express.git
   cd Vercel-Serverless-Function-Express
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Commit to your GitHub repository:**

   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

4. **Deploy on Vercel:**

   - Go to [Vercel](https://vercel.com/) and sign in with your account.
   - Select "New Project" and import your GitHub repository.
   - Follow the prompts to deploy your project.

### Usage

Once deployed, you can send requests to your Vercel URL along with the API endpoint. For example:

```
https://your-vercel-url.vercel.app/api/yourEndPoint
```

### Example cURL Command

Here’s an example of a cURL command to send a request with a parameter \`data\`:

```bash
curl -X POST https://your-vercel-url.vercel.app/api/yourEndPoint \
  -H "Content-Type: application/json" \
  -d '{"data": "Message to express server"}'
```
