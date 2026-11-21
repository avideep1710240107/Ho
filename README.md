# DM Studio — static deploy

Deploy this folder directly to Vercel, Netlify, or another static host. `index.html` is self-contained; there is no build step and no server function is required.

## AI setup
Open a conversation → Info → API Settings. Choose Gemini or OpenAI and paste an API key. The key is stored in this browser's localStorage and requests go directly from this browser to the provider. Without a key, the app uses local offline replies.

**Security:** browser-stored API keys are not secret. This mode is intended for personal/private testing. Do not publish a deployment where visitors can enter or share a key they expect to remain confidential. For a public multi-user site, proxy AI requests through a server-side function and keep the provider key in the host's encrypted environment variables.

## Local storage and expiry
Conversation text is stored in localStorage; compressed photos and videos are stored in IndexedDB. Messages and media are pruned after 24 hours when the app opens and periodically while it remains open. Browser storage expiry is best-effort, not guaranteed secure erasure.

## Notes
The app is an Instagram-inspired fictional DM simulator, not an Instagram client. It does not connect to Instagram accounts or real messages. Demo Reel videos and photo fallback images are remote sample assets; provide your own licensed assets for production use.
