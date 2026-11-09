# J.A.R.V.I.S.

A free, installable AI voice assistant with an Iron Man-inspired HUD. Talk or type, and it answers out loud. Powered by Google Gemini. Bring your own free API key.

**Live app:** https://ia809.github.io/Jarvis/

---

## Features

- **Voice input:** tap the microphone and just talk.
- **Spoken replies:** JARVIS answers out loud (can be turned off in Settings).
- **Futuristic HUD:** animated arc reactor that changes color and speed depending on whether it is listening, thinking, or speaking.
- **Conversation memory:** it remembers the context of your chat.
- **Local history:** your chats are saved only on your own device.
- **Installable (PWA):** add it to your home screen and use it like a normal app.
- **Customizable:** change the personality, model, voice, and colors.
- **Export chat:** download your conversation as a text file.
- **No backend:** everything runs in your browser.

---

## Getting started

### 1. Get a free API key
1. Go to https://aistudio.google.com
2. Sign in with your Google account.
3. Tap **Get API key** and then **Create API key**.
4. Copy the key.

### 2. Open the app
Open https://ia809.github.io/Jarvis/ in Chrome.

### 3. Configure it
1. Tap **SETTINGS**.
2. Paste your API key.
3. Enter a Gemini model name (see below).
4. Tap **SAVE**.

### 4. Talk to it
Tap the microphone, allow microphone access, and speak. Or type in the box and tap **SEND**.

### 5. Install it as an app
In Chrome, tap the menu (three dots) and choose **Install app** or **Add to Home screen**.

---

## Choosing a model

Model names change over time, and some are removed or limited for new accounts. If you get a "model not found" or "no longer available" error:

1. Open this address in your browser, replacing `YOUR_KEY` with your key:
   `https://generativelanguage.googleapis.com/v1beta/models?key=YOUR_KEY`
2. Look for a model whose name contains `flash` and that lists `generateContent` in its supported methods.
3. Copy the name without the `models/` prefix and paste it in **SETTINGS > Model**.

Avoid models with `tts`, `image`, `embedding`, or `live` in the name, since they are not meant for text chat.

---

## Customization

- **Personality:** edit the text in SETTINGS to change how JARVIS talks.
- **Voice replies:** toggle them on or off in SETTINGS.
- **Colors and style:** open `index.html` and edit the variables at the top of the `<style>` section (`--acento`, `--acento2`, `--fondo`, and so on).

---

## Privacy and security

- Your API key is stored **only in your own browser** (localStorage). It is never uploaded to this repository.
- Your messages go directly from your device to Google's Gemini API.
- Voice recognition in Chrome may be processed by Google's servers.
- The free Gemini plan may use your data to improve Google's products, so **do not share private or sensitive information**.
- Never paste your API key into the code, screenshots, or public posts. If it gets exposed, delete it at aistudio.google.com and create a new one.

---

## Known limitations

- Free models can be busy and return a "high demand" error. Wait a moment or switch models.
- The free plan has rate limits per minute and per day.
- Speech recognition works best in Chrome.
- Voice and available languages depend on your device.

---

## Roadmap

Future updates are planned:

- Image generation
- Automatic retries and fallback models
- Model selector with a list of available models
- More themes and customization options
- Language selector for voice input and output

---

## Project structure

| File | Purpose |
|---|---|
| `index.html` | The whole app (interface, styles, and logic) |
| `manifest.json` | Makes the app installable |
| `sw.js` | Service worker for installation and caching |
| `icon.svg` | App icon |

---

## Run it locally

1. Download or clone this repository.
2. In the project folder, start a simple server, for example `python3 -m http.server 8000`.
3. Open `http://localhost:8000` in your browser.

---

## Contributing

Ideas and suggestions are welcome. Open an issue to share feedback or report a bug.

---

## Disclaimer

This is an independent fan project inspired by the fictional J.A.R.V.I.S. It is not affiliated with Marvel, Disney, or Google. Use your own API key and follow Google's terms of service.
