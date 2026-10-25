# Xbox 360 Netplay Server

OpenPak's Xbox 360 Netplay Server.

| | |
| --- | --- |
| Network | Xbox 360, through the Xenia emulator |
| Role | Web API for Xbox 360 online and multiplayer: sessions, players, leaderboards and title storage |
| Depends on | MongoDB |
| Based on | [Xenia Web Services](https://github.com/AdrianCassar/Xenia-WebServices) (MIT) |
| Licence | MIT |

## What it serves

| Endpoint | What |
| --- | --- |
| `/title/:titleId/sessions` | Session create, search, join, leave, migrate, QoS, context, properties and leaderboards |
| `/title/:titleId/servers`, `/services`, `/ports` | Per-title server, service and port lists |
| `/players`, `/leaderboards` | Player presence, user search and settings; leaderboard find, enumerate and rank estimate |
| `/xstorage` | Clips and user and title file storage |
| `/whoami`, `/DeleteSessions` | XNet identity and session cleanup |
| `/sessions` | Aggregated session listing |

## Run

```sh
cp .env.template .env                 # MongoDB must be reachable at MONGO_URI
npm install && npm run build && npm start   # frontend: http://127.0.0.1:36000/
```

## Docs

- [Protocol](docs/protocol.md)
- [Evidence](docs/evidence.md)
- [Deploy](docs/deploy.md)
- [Notes](docs/notes.md)
- [Upstream README](docs/upstream.md)

## Licence

MIT. See [LICENSE](LICENSE).
