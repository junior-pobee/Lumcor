# Lumcor

Lumcor is a messaging and connection platform in development, designed around direct conversations, groups, status updates and personal connections.

## Current foundation

- Responsive messaging interface for desktop and mobile
- Local preview conversations with message sending
- Create direct-chat and group conversation spaces
- Search conversations
- Delete a conversation from the current device
- Status updates in local preview mode
- Light and dark appearance
- Display-name settings and local preview-data reset

## Run

Open `index.html` in a browser or publish the repository with GitHub Pages.

## Important implementation status

This first version is a front-end preview. Data is stored in the browser on the current device. It does not yet provide real accounts, cross-device message delivery, contact discovery, connection requests, synced groups, read receipts, push notifications, or voice/video calls.

Those capabilities require a secure backend. The next integration step is to connect Lumcor to its own Supabase project, configure authentication and database policies, and implement realtime messaging and storage. Never put a Supabase service-role key in browser code.

## Stack

- HTML
- CSS
- Vanilla JavaScript
