# OpenPak integration

OpenPak fork of [Xenia Web Services](https://github.com/AdrianCassar/Xenia-WebServices),
under its existing MIT license. OpenPak changes use `main`.

This is an emulator-oriented REST API. It is not the native Xbox Live protocol
and does not replace OpenPak's x360-kdc, x360-gateway or other native services.

Initial integration work:

- Inventory session, player, storage and leaderboard endpoints used by Wharf.
- Map authenticated OpenPak users to the same stable XUIDs as native Live.
- Review which session functions can share state with native services, and
  explicitly document remaining emulator-only behavior.
- Run isolated tests before enabling routes in production.

The fork is for evaluation. It has not been built, deployed or proven to
interoperate with real Xbox 360 consoles. Upstream title archives and game
assets are separate inputs; do not automatically import them into releases.
