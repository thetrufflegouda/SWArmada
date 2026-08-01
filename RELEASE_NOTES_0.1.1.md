# SWArmada 0.1.1

Version 0.1.1 makes it much easier to find another commander and start an
online match.

## Worldwide player list

- Added an opt-in player list to the right side of the main menu.
- Players choose their own username and receive an automatic, stable
  `#NNNN` identifier.
- No Unity account, password, or account setup is required; authentication is
  anonymous and cached locally.
- Online and in-match states update through Unity Multiplayer Services.
- Your chosen name and anonymous identity persist across game updates on the
  same computer.

## Direct match invitations

- Available players can be invited directly from the worldwide player list.
- Sending an invitation creates the same private Relay-backed lobby used by
  the existing host/join-code flow.
- Accepting an invitation joins that lobby without manually copying a code.
- Player handles now carry into the online lobby and chat.
- Manual hosting and join codes continue to work normally.

## Update notifications

- The game now checks the latest GitHub Release once during startup.
- When a newer semantic version is available, an in-game notification shows
  the installed and available versions.
- The notification includes a button that opens the release page on GitHub.
- A failed or unavailable update check never blocks the game from starting.

## Download

Download `SWArmada-0.1.1-Windows-x64.zip`, extract the entire archive, and run
`SWArmada.exe`.

SHA-256:

`1235AE580266B03EFDAADC51A7F3DB4E67209DCD4FA5DA406F4ACD20BE771306`
