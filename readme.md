Project 3 — Real-Time Team Collaboration Application
Priority: P1 — Build if you want stronger frontend and real-time engineering evidence.

Create a team application with real-time messaging, presence, and collaboration.
Stack
- Next.js, React, TypeScript.
- Node.js.
- WebSockets, using Socket.IO or a suitable WebSocket implementation.
- PostgreSQL.
- Redis for shared state or cross-instance messaging where appropriate.
- Docker.
- GitHub Actions.
- Playwright and integration tests.
Architecture
Next.js Client
      |
      | HTTPS / WebSocket
      v
Node.js API + WebSocket Gateway
      |
      +---- Authentication and Authorization
      |
      +---- Conversation Service
      |
      +---- Message Service
      |
      +---- Presence Service
      |
      +---- Notification Service
      |
      +---- PostgreSQL
      |
      +---- Redis

Modules
- Users and memberships.
- Conversations and channels.
- Message history.
- Real-time message delivery.
- Presence and typing indicators.
- Read receipts.
- Notifications.
- Message pagination.
- Reconnection and duplicate-message handling.
Senior-level challenges
Design message identifiers, reconnect behaviour, ordering guarantees, and delivery semantics. Explain what happens when a client loses connectivity or a server instance restarts.

Do not claim exactly-once delivery merely because you use WebSockets. Real distributed systems require careful treatment of retries, duplicates, acknowledgements, and persistence.