# Lumcor

Lumcor is a connected messaging application built around direct conversations, connection requests, groups and short-lived status updates.

## Live foundation

- Supabase email authentication
- User profiles and unique usernames
- Connection requests and acceptance
- Direct conversations for accepted connections
- Group creation and member invitations
- Realtime text message delivery
- Status publishing and online-only status viewing
- Row Level Security on all public application tables
- User blocking checks for new connection requests, messages and status visibility
- Offline access to previously cached conversations
- Offline sending and status actions are disabled
- Service worker caching for the application shell
- Light and dark appearance
- GitHub Pages deployment through GitHub Actions

## Backend

Lumcor uses its own Supabase project. The browser uses only the publishable key; no service-role or secret key is included in the repository.

## Offline and data use

Previously loaded messages are cached in IndexedDB for offline reading. New messages, connection actions, group changes, and status publishing or viewing require an internet connection. Realtime updates arrive when the user is online again.

The target is to keep a typical text message's application data very small. A 2 KB target can apply to the compact message record, but total network use also includes HTTPS, authentication and realtime protocol overhead, so a full send/receive operation cannot be guaranteed to stay under 2 KB.

Media sharing, voice/video calls, push notifications, and full message delivery receipts are not implemented yet.

## Run

Open `index.html` in a browser or deploy with GitHub Pages.

## Stack

- HTML
- CSS
- Vanilla JavaScript
- Supabase Auth, Postgres and Realtime
- IndexedDB
- Service Worker
