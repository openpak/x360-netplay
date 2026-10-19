# OpenPak status: excluded from integration

This is an evaluation fork of
[Xenia Web Services](https://github.com/AdrianCassar/Xenia-WebServices), under
its existing MIT license. It is not an active OpenPak service.

OpenPak requires one native Xbox 360 backend shared by physical consoles and
Wharf. Xenia Web Services uses an emulator-specific REST API and is therefore
excluded from the implementation plan. Do not build, deploy or add an adapter
to it as part of the Xbox 360 work.

The fork remains as evaluation history. The production path is OpenPak's
native x360 services. Wharf must emulate the console's XAM/XNet behavior and
speak the same native service protocols, identities and session contracts as
physical Xbox 360 hardware. Compatibility work belongs in Wharf or the shared
native services, without a separate emulator-only protocol.
