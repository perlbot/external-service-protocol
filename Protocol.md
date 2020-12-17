Glossary
--------

Client - The external service implementation, i.e. a bridge to Discord or Matrix
Server - The main part of the bot itself, that implements all the plugins and manager etc.


Message Types
-------------

1. Message
  1. Incoming (Client -> Server)
  2. Outgoing (Server -> Client)
  3. Announcement (Client -> Server -> Client) i.e. the pastebin
2. User State Change
  1. Joined channel
  2. Parted channel
  3. Permissions changed
  4. State change (Away, present, disconnected, etc.)
3. Channel State Change
  1. Topic change
  2. Pinned message
  3. Announcement changes (Allow, Disallow, etc.)
4. Client/Server Introspection
  1. Server Asks Client (Client gives channel list, server name, etc.)
  2. Client Ask Server (Server gives connected client list, server names, etc.) i.e. mostly for the pastebin to automagically get channel lists
  3. Server stats (Uptime, message rates, etc.0
5. 
