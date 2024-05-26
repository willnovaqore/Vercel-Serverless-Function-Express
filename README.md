# Vercel Serverless Function Template 2024

This repository contains a simple Vercel serverless function template for 2024. It is designed to work out of the box and to be a starting point for deploying serverless functions on Vercel.

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

You can change the \`yourEndPoint\` to anything you would like, and the API call endpoint will update to whatever you called it. For example, if you rename the file to \`newEndPoint.js\`, your URL will be:

```
https://your-vercel-url.vercel.app/api/newEndPoint
```

### Adjusting Server Timeout

You can adjust the server timeout for any route by modifying the \`vercel.json\` file. Here is what the \`vercel.json\` looks like:

```json
{
    "version": 2,
    "rewrites": [
        {
            "source": "/(.*)",
            "destination": "/api"
        }
    ],
    "functions": {
        "api/yourEndPoint.js": {
            "maxDuration": 60
        }
    }
}
```

- Replace \`yourEndPoint.js\` with your endpoint file name.
- Adjust the \`maxDuration\` parameter to set the timeout (in seconds) for each endpoint.
- Note that Vercel has different max durations for their paid and non-paid plans. Please refer to [Vercel's documentation](https://vercel.com/docs/concepts/functions/edge-functions/edge-functions#limits) for more details on the limits.

### Example cURL Command

Here’s an example of a cURL command to send a request with a parameter \`data\`:

```bash
curl -X POST https://your-vercel-url.vercel.app/api/yourEndPoint \
  -H "Content-Type: application/json" \
  -d '{"data": "Message to express server"}'
```
