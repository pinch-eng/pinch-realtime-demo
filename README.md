## NodeJS Pinch Starter

[![Documentation](https://img.shields.io/badge/docs-startpinch.com-blue.svg)](https://docs.startpinch.com)

A minimal web app that demonstrates Pinch real-time speech translation.

## Requirements

- **Node.js 18+**
- A Pinch API key

## Setup

1. Clone this repository:

```bash
git clone https://github.com/pinch-eng/real-time-demo-app.git
cd real-time-demo-app
```

2. Set your API key in a `.env` file in the project root:

```
PINCH_API_KEY=your_api_key_here
```

Get your API key in the [Pinch Developer Portal](https://portal.startpinch.com/dashboard/developers).

3. Install dependencies and start the server:

```bash
npm install
npm start
```

4. Open the demo at [http://localhost:3000](http://localhost:3000).

## Usage

- Click **Connect** to create a session and start streaming your microphone audio.
- Original transcripts appear on the left; translated transcripts on the right.
- The timer at the top shows how long the session has been active.
- Click **Disconnect** to end the session.

## How It Works

1. The browser sends a request to the local Express server (`/api/session`).
2. The server proxies the request to the Pinch API with your API key and returns a `url` and `token`.
3. The browser connects to the room, publishes your microphone audio, and listens for transcript data messages.
4. Transcripts are displayed in real time, split into original and translated columns.

## Support

For any issues, contact `support@startpinch.com`.

## Getting Help

- [Read our Docs](https://docs.startpinch.com)
- [Join our Discord](https://discord.gg/s8KFeXpP)
- [Reach out on LinkedIn](https://www.linkedin.com/company/startpinch)
- [Reach us on X](https://x.com/StartPinch)
