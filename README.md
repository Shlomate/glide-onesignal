# Glide + OneSignal Push Notification Page

This is a minimal static site to register users for push notifications via OneSignal and send their `player_id` back to Glide using a Make webhook.

## Files

- `public/index.html` – Loads OneSignal and triggers registration
- `public/OneSignalSDKWorker.js` – Required service worker
- `public/OneSignalSDKUpdaterWorker.js` – Required service worker
- `vercel.json` – Optional: removes .html from URLs

## Usage

1. User opens this page via a link in your Glide app (`?uid=abc123`)
2. The browser asks for push permission
3. OneSignal returns a `player_id`
4. The page sends `{ uid, pid }` to a Make webhook
5. You store the player ID in Glide and can now send push messages!
