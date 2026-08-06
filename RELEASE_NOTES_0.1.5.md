# SWArmada 0.1.5

Version 0.1.5 is a multiplayer, deployment, and messaging maintenance release.

## Multiplayer and deployment

- Fixed multiplayer startup for legal custom fleets containing huge ships such
  as the Executor-class Star Dreadnought. Match staging and host validation now
  use the resolved gameplay footprint, preventing the battle from opening in a
  non-interactive prototype state.
- Standard Front deployment now keeps capital ships within Distance 5 of the
  left and right board edges.
- Squadrons may deploy anywhere on the board when their complete base is within
  Distance 2 of a friendly ship.
- Capital ships may deploy as close together as desired while their bases do
  not overlap.

## Presentation and rules feedback

- Interdictor Grav Well tokens show a faint Distance 3 ring on hover and use
  the same token-to-base measurement for their setup effect.
- Already-activated ship rings render below ship models again so camera angle
  cannot hide them inside the hull.

## Direct messages

- Player names open direct messages with one click, and the persistent dock is
  now labeled `MESSAGES`.
- Message drafts support up to 500 characters in a two-line, wrapping,
  scrollable composer that follows the caret while typing.
- Displayed messages wrap and the transcript scrolls normally as history grows.
- Opening `MESSAGES` after receiving a DM selects the conversation containing
  the latest unread message.

## Platforms and updating

- Updated Windows x64, Linux x86-64, and Universal macOS builds are included.
- Existing 0.1.4 installations will be offered 0.1.5 through the automatic
  update notice.

## Downloads

- `SWArmada-0.1.5-Windows-x64.zip`
- `SWArmada-0.1.5-Linux-x86_64.tar.gz`
- `SWArmada-0.1.5-macOS.tar.gz`

The Windows and macOS builds are not code-signed or notarized. SHA-256 sidecar
files are included with every archive.
