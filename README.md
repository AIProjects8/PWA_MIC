# Voice Recorder PWA

A Progressive Web App (PWA) for recording and playing back audio.

## Features

- Record audio using device microphone
- Play back recordings
- Works offline
- Installable as a mobile/desktop app
- iOS and Android compatible

## Prerequisites

Make sure you have the following tools installed:

- **Node.js** (with npm)
- **Live-server** (for serving your app locally)
- **Ngrok** (to expose your local server over HTTPS)

### Install the required tools

1. **Install Live-server**

   To install `live-server` globally, run the following command in your terminal:

   ```bash
   npm install -g live-server
   ```

2. **Install Ngrok**

   To install `ngrok` globally, run:

   ```bash
   npm install -g ngrok
   ```

## Setting Up the Development Environment

### Step 1: Start the Local Server

1. Navigate to the directory where your PWA project is located.
2. Start the `live-server` on port 5500 by running the following command:

   ```bash
   live-server --port=5500
   ```

   This will serve your project on `http://localhost:5500`.

### Step 2: Expose the Local Server Using Ngrok

1. Open a new terminal window and run the following command to expose your local server over HTTPS using `ngrok`:

   ```bash
   ngrok http 5500
   ```

   After running this command, you should see an output like this:

   ```bash
   Forwarding                    https://1ee6-88-156-104-188.ngrok-free.app -> http://localhost:5500
   ```

   Copy the **HTTPS URL** provided (e.g., `https://1ee6-88-156-104-188.ngrok-free.app`).

### Step 3: Test the PWA on Your Phone

1. Open the HTTPS URL (provided by `ngrok`) in a mobile browser on your phone.
2. Once the page loads, you can install the PWA on your phone by following these steps:

   - On **Android**: When you visit the site, the browser will prompt you with an option to **Add to Home screen**. Tap on it and follow the prompts.
   - On **iOS**: Open Safari, visit the URL, and tap the **Share** button at the bottom of the screen. From the options that appear, tap **Add to Home Screen**.

3. Your PWA will now be installed on your phone and accessible offline once cached via the service worker.

## Troubleshooting

- **SSL/TLS Certificate Issues**: If you encounter issues related to HTTPS or SSL/TLS, make sure your certificate is valid, or check for mixed content errors in your browser's developer tools.
- **Service Worker Not Caching**: Ensure your service worker is correctly set up and registered in the PWA. Check for any errors in the browser console.
- **Ngrok Free Limitations**: The free version of ngrok may disconnect after a period of time. You can restart `ngrok` if this happens.

## Conclusion

With `ngrok`, `live-server`, and the steps above, you can easily test and install PWAs on your mobile device directly from a local development server.
