# Changelog

This changelog preserves the complete notes from every published SWArmada
release, newest first. Downloads and their original release descriptions remain
available under [GitHub Releases](https://github.com/thetrufflegouda/SWArmada/releases).

## [0.2.3](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.2.3) - 2026-08-28

SWArmada 0.2.3 is a battle-flow, rules, inspection, and combat-presentation repair release built from the latest live playtests.

### Fixed

- Fixed the Haor Chall reaction path that could leave a ship stuck after firing at a squadron and committing movement.
- Corrected ship-to-ship hull-zone targeting and line of sight to use the physical base geometry, including legal nose-to-nose front-zone attacks.
- Corrected special ignition weapons to use each weapon's own printed arc and range. Attack planning now shows the exact token-centered reach as a solid amber overlay, while token placement uses a clean dashed maximum-range cap.
- SPHA-T now reduces the ship's effective Squadron value everywhere it is presented and resolved.
- Squadron Brace, Scatter, and Evade choices now go directly to the exact physical token instead of opening a redundant extra menu. AI squadrons also spend useful defense tokens when available.
- Corrected Reactive Gunnery, Salvo, close-range Evade, Demolisher and Engine Techs, Navigate-command timing, Beck command timing, and Centicore Relay interactions.
- Command dials now commit with one click and retain the intended selection during the dial animation.
- Squadron commands report the number of currently eligible squadrons in range or through Relay, clearly track activations, and provide an explicit skip action.
- Enemy units remain inspectable during the other player's turn without submitting an illegal activation command.
- Ship shield pips and spatial condition information remain available through command, attack, targeting, and waiting states. The attacking ship's own shield pip no longer flashes as duplicate combat feedback.
- Squadron movement, displacement, and attack targeting now share the same legal-range cues, overlap protection, and faction-coloured presentation.
- Attack participants, defense tokens, upgrade abilities, selected dice effects, and accepted critical effects are shown more clearly to both players during resolution.
- Restored reliable ship and squadron laser beams, including Republic green capital-ship fire and Separatist red capital-ship fire; Clone Wars squadrons use red fire.
- Corrected attack and dogfight camera tracking, ship-activation framing, movement easing, faction-coloured selection glows, squadron base rendering, and combat overlays.
- Refined compact action-button borders, non-scrolling transient instructions, attack-resolution layout, fleet-management headings, and critical-effect wording.

### Verification

- Unity editor assembly compiled with 0 errors.
- Battle Presentation, Attack Interaction, Attack Range, AI Foundation, Playtest Recorder, Android Touch and Placement, official timing repairs, current combat fixes, open-issue repairs, and all 44 Clone Wars checks passed.
- Clean non-development builds: Windows x64, Linux x86-64, macOS Universal, Android ARM64.
- Packaged scenes: MainMenu and Battle_Default only.
- Android: ARM64, version code 6, Android 8.0 / API 26 minimum.
- Windows packaged-player startup smoke passed.
- SHA-256 sidecars and SHA256SUMS.txt are attached.

## [0.2.2](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.2.2) - 2026-08-26

SWArmada 0.2.2 is a focused gameplay and inspection hotfix.

### Fixed

- Squadrons can no longer end a move with positive-area base overlap against another squadron or ship. Bases that merely touch remain legal.
- The overlap rule now applies consistently to player movement, AI movement, special card-effect movement, and host-authoritative online/replay validation.
- Ending squadron targeting no longer lets a stale squadron selection erase the active ship's shield pips and spatial condition display.
- The condition wrench now restores the active ship and remains responsive after those targeting transitions.

### Verification

- Unity editor assembly compiled with 0 errors.
- AI and squadron-movement verification passed, including overlap, touching, AI routing, and host-authority regressions.
- Focused spatial dossier verification passed, including shield-pip persistence and wrench interaction.
- Clean non-development builds: Windows x64, Linux x86-64, macOS Universal, Android ARM64.
- Packaged scenes: MainMenu and Battle_Default only.
- Windows packaged-player startup smoke passed.
- Android: ARM64, version code 5, Android 8.0 / API 26 minimum.
- SHA-256 sidecars and SHA256SUMS.txt are attached.

## [0.2.1](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.2.1) - 2026-08-26

SWArmada 0.2.1 is a focused fleet-builder rules fix.

### Fixed

- Custom fleet limits now work correctly when equipping upgrades above 400 total points.
- The upgrade picker now honors the fleet's selected Custom point limit while continuing to enforce upgrade slots, faction restrictions, uniqueness, and card restrictions.
- Official Standard remains fixed at 400 fleet points and 134 squadron points.
- Fleet budget calculations continue to use the actual combined cost of ships, upgrades, and squadrons; squadron points are not reserved.

### Verification

- Fleet-core verifier: 25/25 passed.
- Clean non-development builds: Windows x64, Linux x86-64, macOS Universal, Android ARM64.
- Packaged scenes: MainMenu and Battle_Default only.
- Android: ARM64, version code 4, Android 8.0 / API 26 minimum.
- SHA-256 sidecars and SHA256SUMS.txt are attached.

## [0.2.0](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.2.0) - 2026-08-26

Version 0.2.0 is the Clone Wars, VS AI, rules-correction, battle-input, and
cross-platform release. It adds the Galactic Republic and Separatist Alliance,
expands solo play across all four factions, and includes a large reliability
pass for squadrons, cards, multiplayer recovery, touch controls, inspection,
camera behavior, and combat presentation.

### Republic, Separatists, and fleet content

- Added the Galactic Republic and Separatist Alliance as supported factions
  throughout fleet building, battle setup, rules resolution, AI, replay, and
  multiplayer.
- Added official Clone Wars ships, squadrons, commanders, officers, titles,
  weapons teams, ordnance, defensive upgrades, and faction-specific effects.
- Added curated legal showcase fleets for Rebel, Imperial, Republic, and
  Separatist play at 400/399/400/399 points. Existing user fleets and edited
  starter copies remain untouched.
- Added correct Huge-ship setup behavior: the complete oriented base remains in
  the setup area, touches its owner's edge, and re-anchors through rotation.
- Expanded rules support for Ahsoka Tano, SPHA-T, Ordnance Pods, Jedi Hostage,
  General Grievous, Invisible Hand, Sa Nalaor, Resolute, Tranquility, Raddus,
  Profundity, Salvo, Gunnery Team, Sato, and many other card interactions.

### VS AI and playtest diagnostics

- Added Player vs AI from the Single Player menu. Computer players can command
  all four factions through deployment, commands, ship movement, attacks,
  squadron activations, defense choices, objectives, and card decisions.
- AI deployment and movement now use deterministic match-seeded scoring for
  firing lanes, friendly separation, future maneuver freedom, objective goals,
  legal squadron routes, and play-area safety.
- Fixed decision ownership leaks that could hand an AI choice to the player or
  let a stale modal survive into another unit's activation.
- Fixed AI stalls during Squadron commands and squadron movement, including
  destination submission, no-choice defense windows, extra attacks, and nested
  triggered abilities.
- Added bounded local PlaytestRecords with decision-owner, command, geometry,
  dice, seed, attack-phase, and stall evidence for reproducible bug reports.
  Recorder data is local diagnostics only and is not part of network/replay DTOs.

### Squadron, attack, and card-rule repairs

- Relay now uses its correct activation-capacity rules. Reserve Hangar Decks can
  skip or return a legal non-unique Swarm squadron without softlocking combat.
- Squadron anti-ship damage is target-correct: non-Bomber criticals do not harm
  ships, Bomber criticals do, and normal hit icons from X-wing, Y-wing, A-wing,
  and other pools resolve correctly against capital ships.
- Defense-token commands preserve the exact physical ready/exhausted copy.
  Sloane, Intel Officer, NK-7, Accuracy, TRCs, Salvo, ECM, and other effects can
  exhaust or discard the intended token without duplicate-token ambiguity.
- Redirect now blocks an invalid defending zone with no shields and lets the
  defender choose the adjacent hull zone and exact transferable amount.
- Ordinary flak and Ordnance Pods can select every desired legal squadron in the
  chosen arc, then resolve independent deterministic rolls and defense windows.
- Salvo against squadrons uses the ship's printed anti-squadron armament and
  normal accuracy/defense timing. Gunnery Team enforces its same-defender limit
  across the full activation, including extra anti-squadron attacks.
- Corrected Hera Rogue timing, Salvation critical damage, dial-plus-token
  Concentrate Fire, Raddus/Profundity storage and placement, attack obstruction,
  huge deployment, shield maximums, and many additional timing gates.

### Battle input on desktop and Android

- Squadron selection remains reversible until a move or attack is actually
  committed. Back or another ready friendly squadron safely releases the
  provisional choice and rolls back provisional Relay/ability state.
- Illegal squadron movement releases reset the model, destination marker,
  attack envelope, and touch ownership immediately so the player can retry
  without reopening Move.
- Squadron movement keeps a live faction-colored attack envelope at every
  staged destination, including Snipe and Major Rhymer range changes.
- Android deployment ships and squadrons grab immediately with generous touch
  targets. Direct placement/movement owns the active finger and no longer pans
  the camera underneath the unit.
- Quick empty-board drag pans; hold-then-drag opens the unit-locator marquee.
  Dense unit hitboxes hand ordinary drags back to the camera after tap slop, so
  close zoom can still pan.
- Fixed retained-touch command spam, misleading selection rejections, dossier
  close behavior, accidental mobile hover tooltips, command-dial swipes, and
  software-keyboard access to match chat.
- Command planning keeps the ship highlighted until its dial is committed, and
  the live command description updates with every physical dial change.

### Inspection, camera, and battle presentation

- Public ship and squadron inspection remains available during every gameplay
  state, including AI/hotseat waiting, targeting, ignition, movement, and modal
  decisions, without dispatching unintended gameplay commands.
- The dossier and three above-unit inspection diamonds follow the complete
  rendered hull bounds, remain above the public-information layer, and preserve
  the selected attack source/defender relationship.
- Rebuilt the radar-mounted weapon readout as direct printed CLOSE/MID/LONG dice
  tallies for anti-ship and flak instead of confusing cumulative values.
- Improved automatic camera framing, squadron dogfight presentation, hit/miss
  feedback, attack-cinematic recovery, multi-target flak feedback, command
  descriptions, fleet-card shield displays, and unit-locator behavior.
- Baked the shared CRT profile for real battle scenes: native Pixel Size 0,
  point filtering, tuned RGB/scanline/aberration/brightness/contrast, and the
  editor-only visual tuner excluded from packaged players.

### Multiplayer, lobbies, presence, and chat

- Relay connection hiccups now pause the battle, reconnect the existing Unity
  session, restore the authorized Player 2 identity, and replay accepted command
  history from the last received revision instead of falling into a static or
  local-hotseat state.
- Hardened command ownership so replacement or stale clients cannot submit as
  Player 2, and catch-up/rejection responses return to the exact sender.
- Improved typed-presence recovery, handle updates, invitation/lobby isolation,
  stale heartbeat handling, request pacing, and recoverable membership errors.
- Match chat is accessible from a persistent desktop rail or Android GAME CHAT
  tab and shares the wrapped 500-character composer used by lobby and DMs.

### Downloads

- `SWArmada-0.2.0-Windows-x64.zip`
- `SWArmada-0.2.0-Linux-x86_64.tar.gz`
- `SWArmada-0.2.0-macOS.tar.gz` (universal x86-64 + Apple silicon)
- `SWArmada-0.2.0-Android-arm64.apk` (Android 8.0 / API 26 minimum)

The Windows and macOS players are not code-signed or notarized. The Android APK
uses a sideload/test signature rather than Play Store signing. SHA-256 sidecars
and a combined `SHA256SUMS.txt` are included.

Every player contains exactly the Main Menu and real Battle Default scene. The
editor-only prototype, generated backup folders, Burst debug data, `DoNotShip`,
logs, symbols, scratch files, private diagnostics, and patch-note source files
are not included in any downloadable package.

## [0.1.6](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.6) - 2026-08-14

Version 0.1.6 is the Onager, Android, controls, combat-input, and presentation
release. It also includes substantial multiplayer, chat, lobby, movement, and
rules-correction work shared by every platform.

### Onager and combat rules

- Added the Onager-class Star Destroyer's special firing arc, targeting token,
  ignition attacks, Extreme range, forced first-attack timing, Cataclysm timing,
  and official Onager upgrade interactions.
- Ship attacks now determine firing-arc legality from the physical defending
  hull-zone edge. Targeting anchors remain line-of-sight references, so a clear
  front-to-front shot is no longer rejected because an authored anchor sits
  outside the base.
- Attack damage is counted from hit and critical icons. Accuracy and blank faces
  remain zero-damage unless a printed card effect explicitly converts them.
- Corrected close-range Evade availability, Redirect allocation, Auxiliary
  Shields Team capacity, and exact duplicate defense-token handling.
- NK-7 and Intel Officer now preserve the exact physical defense token through
  local and accepted online commands. Intel Officer shows only the current
  opposing defender's tokens and uses compact token labels.
- The Escort VIP ship is restricted to Navigate commands and tokens.

### Stable attack and movement input

- Attacking now follows one consistent flow: select a source firing arc, select
  a defending hull zone, then commit. Either selection can be changed before
  committing, while body taps, empty taps, and invalid taps leave both choices
  intact.
- Close or overlapping ships use the visibly nearest curved hull-zone control,
  preventing a defender tap from silently switching the attacker's firing arc.
- Cannon-mode touch input no longer falls through into battlefield selection,
  flash closed, or leave second-attack targeting in a stale state.
- Ram previews retain the complete plotted maneuver: reachable travel is cyan,
  the impossible remainder is grey, and the real landing choice is orange.
- HALT TO ZERO uses the same orange maneuver arrow as desktop, raised above the
  ship's size-aware hull hitbox so it remains visible and clickable.
- Squadron selection, targeting, movement, and collision displacement were made
  reliable on touch. Accepted movement now completes before the turn advances.

### Android

- Added the first Android ARM64 player build, using the same battle rules and
  content as desktop. Minimum supported version is Android 8.0 / API 26.
- Android uses the device's native landscape resolution; only the frame-rate
  limit is configurable.
- Added one-finger camera pan with a deliberate deadzone and inertial glide,
  two-finger twist/orbit, two-finger pitch, and more responsive pinch zoom.
- Scrollable menus accept inertial swipes across the full list surface. Fleet
  and map-builder palette entries are armed with a tap and placed with a later
  map tap, so list scrolling no longer starts an accidental drag.
- World placements stage before confirmation. Squadron displacement supports
  immediate touch-drag, and firing-arc selection exposes all four touch targets.
- Added touch-accessible in-game Menu and Game Chat controls, safe-area layout,
  the desktop game icon, visible 3D ship/obstacle models, and logcat-only error
  reporting instead of an on-screen development console.
- Replaced unreliable dossier gestures with a spatial notepad diamond above
  ships and squadrons. Single tap selects and quick double-tap focuses.

### Controller and controls

- Rebuilt controller support around one persistent virtual cursor: right stick
  moves the cursor, D-pad navigates exposed controls, A or right trigger clicks,
  and B closes the top visible surface before routing to gameplay Back.
- Left stick pans, LB/RB orbit, LT plus vertical left stick zooms, and L3 frames
  the whole table. The upper analog curve reaches Shift-keyboard speed without
  sacrificing low-stick precision.
- Rebuilt the virtual keyboard with a live wrapped input field, lowercase
  default, L3 caps, one-shot/double-latch Shift, and letter/symbol pages.
- The shared Controls reference is available directly from the main menu,
  Options, and the in-game pause menu.

### Squadrons and battle presentation

- Squadron attack runs are substantially slower: fighters approach, keep moving
  while swarming the target, fire, and return to their exact formation slots.
  Anti-ship attacks, anti-squadron attacks, and Counter share this presentation.
- Added an attacker-mounted combat camera which keeps the defender in view,
  holds through combat feedback, restores the exact prior view, and yields
  immediately to real player camera input.
- Ship lasers now originate from the visual center of the firing ship.
- Contextual ship-base outlines appear during deployment, movement, targeting,
  displacement, and other footprint-dependent decisions.
- Hull-zone indicator lines now curve subtly inward, while their endpoints and
  all authoritative rules geometry remain unchanged.
- Improved maneuver markers, firing arcs, targeting-token orientation, ship
  selection over visual hulls, dice-chip layout, and desktop menu text sizing.
- Baked the tuned CRT/PSX profile, including forced point filtering and reduced
  random wear/tear.

### Lobbies, multiplayer, and chat

- Added request coordination, pacing, retry, and stale-presence handling to
  reduce Lobby Service rate-limit bursts during connect, invite, and chat flows.
- Isolated simultaneous presence/chat and match-lobby event caches to prevent
  lobby callback corruption and the repeated lobby error cascade.
- Reworked local and online lobby setup with framed game-type arrows, a separate
  Starting Options row, compact two-way choices, and clear gold active states.
- Lobby, direct-message, and in-game chat now share 500-character wrapping,
  scrolling composers and reliable bottom autoscroll.
- Direct messages use top conversation tabs for opened, historical, or unread
  contacts instead of cycling through unrelated players.

### Downloads

- `SWArmada-0.1.6-Windows-x64.zip`
- `SWArmada-0.1.6-Linux-x86_64.tar.gz`
- `SWArmada-0.1.6-macOS.tar.gz`
- `SWArmada-0.1.6-Android-arm64.apk`

The Windows and macOS builds are not code-signed or notarized. The Android APK
uses a sideload/test signature rather than Play Store signing. SHA-256 sidecars
and a combined `SHA256SUMS.txt` are included. Generated backup, Burst debug,
`DoNotShip`, log, and symbol folders are not part of any download.

## [0.1.5](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.5) - 2026-08-06

Version 0.1.5 is a multiplayer, deployment, and messaging maintenance release.

### Multiplayer and deployment

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

### Presentation and rules feedback

- Interdictor Grav Well tokens show a faint Distance 3 ring on hover and use
  the same token-to-base measurement for their setup effect.
- Already-activated ship rings render below ship models again so camera angle
  cannot hide them inside the hull.

### Direct messages

- Player names open direct messages with one click, and the persistent dock is
  now labeled `MESSAGES`.
- Message drafts support up to 500 characters in a two-line, wrapping,
  scrollable composer that follows the caret while typing.
- Displayed messages wrap and the transcript scrolls normally as history grows.
- Opening `MESSAGES` after receiving a DM selects the conversation containing
  the latest unread message.

### Platforms and updating

- Updated Windows x64, Linux x86-64, and Universal macOS builds are included.
- Existing 0.1.4 installations will be offered 0.1.5 through the automatic
  update notice.

### Downloads

- `SWArmada-0.1.5-Windows-x64.zip`
- `SWArmada-0.1.5-Linux-x86_64.tar.gz`
- `SWArmada-0.1.5-macOS.tar.gz`

The Windows and macOS builds are not code-signed or notarized. SHA-256 sidecar
files are included with every archive.

## [0.1.4](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.4) - 2026-08-05

Version 0.1.4 is a focused multiplayer hotfix following the 0.1.3 maintenance
release.

### Fix

- Fixed capital-ship squadron displacement in multiplayer. Confirming a legal
  squadron placement now remains valid until the host-authoritative command is
  applied, so the game advances correctly after the final displaced squadron
  and continues through additional queued displacement placements.

### Platforms and updating

- Updated Windows x64, Linux x86-64, and Universal macOS builds are included.
- Existing 0.1.3 installations will be offered 0.1.4 through the automatic
  update notice.

### Downloads

- `SWArmada-0.1.4-Windows-x64.zip`
- `SWArmada-0.1.4-Linux-x86_64.tar.gz`
- `SWArmada-0.1.4-macOS.tar.gz`

The Windows and macOS builds are not code-signed or notarized. SHA-256 sidecar
files are included with every archive.

## [0.1.3](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.3) - 2026-08-05

Version 0.1.3 is a small maintenance release following the 0.1.2 objective-mode
update.

### Fixes

- Fixed multi-squadron displacement so placing the first displaced squadron no
  longer clears the pending placement for the second one.
- Fleet Archives now returns to the immediately previous Fleet Management menu
  instead of the main menu.

### Platforms and updating

- Added the first macOS release as a Universal app for Intel and Apple Silicon.
- Added macOS release-archive recognition and SHA-256 verification to the
  in-game updater.
- Windows and Linux 0.1.2 players will be offered 0.1.3 through the existing
  automatic update notice.

### Downloads

- `SWArmada-0.1.3-Windows-x64.zip`
- `SWArmada-0.1.3-Linux-x86_64.tar.gz`
- `SWArmada-0.1.3-macOS.tar.gz`

The Windows and macOS builds are not code-signed or notarized. SHA-256 sidecar
files are included with every archive.

## [0.1.2](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.2) - 2026-08-04

Version 0.1.2 is the objective-gameplay release. It adds three complete custom
scenarios, expands fleet and map setup, introduces fleet-text importing and
persistent direct comms, and includes a broad rules, multiplayer, presentation,
and usability pass.

Republic and Separatist factions are intentionally deferred to version 0.1.3.

### New objective game modes

#### Escort the VIP

- Playable long-approach objective with host-selectable Escort and Interceptor
  roles in online lobbies and the same P1/P2 choice in local hotseat.
- The Escort receives a faction-specific zero-point VIP Transport with its own
  shared combat profile, command behavior, deployment position, and objective
  HUD.
- The Escort wins by surviving to extract the VIP at the end of a round or by
  destroying every Interceptor capital ship. The Interceptor wins by destroying
  the VIP or preventing extraction through Round 10.
- VIP extraction requires the transport's full base inside the Extraction Zone.

#### Seize the Station

- Playable center-station objective with explicit capture-or-continue choices,
  speed-0 capture, contesting, departure handling, and a full-round scoring
  delay.
- Uses the converted Metal station model and its original material groups as a
  static center objective.

#### Intel Retrieval

- Three fixed centerline Intel tokens, Distance 1 hover rings, and a baked
  crashed-Gozanti/debris environment.
- Ships that enter an Intel Zone choose whether to stop and begin downloading
  or continue their plotted maneuver. Grazes stop at the first legal 50% pose;
  pass-through maneuvers stop when fully contained.
- Downloads require speed 0, continued zone overlap, and one full uncontested
  round. A ship may leave and later restart a download normally.
- Only light and medium ships may retrieve Intel. Heavy ships can contest but
  receive a spatial eligibility warning.
- Retrieved tokens shrink and ease onto their carrier, travel with it, and
  detach at the destruction point if the carrier is lost.
- Delivery requires the carrier's full base inside its own starting area and
  resolves at the end of the current round. The first player to deliver two
  tokens wins.

### Scenario and map setup

- Custom maps now store a scenario assignment: Default, Escort the VIP, Seize
  the Station, or Intel Retrieval.
- Fleet Sandbox, local hotseat, and online setup offer maps appropriate to the
  selected scenario.
- Setup screens use a three-column fleet/scenario/fleet layout with objective
  cards shown at their native aspect ratio and a centered hover zoom.
- Escort the VIP and Intel Retrieval always use long-approach deployment.
- Objective matches keep both starting-area outlines visible throughout play.

### Fleet management and rules

- Added an `IMPORT FLEET` workflow for Ryan Kingston and Star Forge text lists,
  including a Save As name, labeled ship sections, `=` upgrade/squadron lines,
  grouped squadron quantities, shorthand ship names, and parenthetical ace
  chassis.
- Import totals are recalculated from the in-game catalog. Unsupported or
  illegal content is skipped with a readable reason instead of corrupting the
  remaining list.
- Fleet Builder now distinguishes `OFFICIAL STANDARD` and `CUSTOM` rules.
  Official mode enforces 400 fleet points and the 134-point squadron limit;
  Custom mode retains editable limits without tournament composition caps.
- Local and online setup include a synchronized Official/Custom Fleet Rules
  switch. The online host controls it, and changing rules clears readiness.
- Fleet cards show capital-ship and squadron point totals, and ship roster
  entries expose a dedicated Upgrades button.
- Local PREVIOUS/NEXT fleet controls now cycle the complete saved archive for
  both players without forcing a full setup-screen redraw.

### Online play, player directory, and comms

- Online presence uses heartbeats and expiry so closed games no longer linger
  as ghost players.
- Match invitations now create and confirm one joinable Relay lobby, tolerate
  modest clock skew, reconcile missed events, and queue arrivals during another
  online operation.
- Added persistent direct messages from the worldwide player list. Double-click
  a player to open a conversation from any front-end screen or battle.
- Direct comms collapse to a single right-edge vertical tab with per-contact
  drafts, session history, and unread counts.
- Chat notification audio now plays only for a genuinely new remote message,
  not local echoes or replayed presence snapshots.
- Online handshakes reject missing or mismatched client versions before a match
  can start.

### Updating

- The startup update notice can automatically download the correct Windows ZIP
  or Linux tarball to the player's Downloads folder.
- Downloads use a unique partial file, verify the published SHA-256 sidecar,
  and promote only a valid archive. Failures remain readable and retryable
  without closing the game.

### Rules and combat improvements

- Squadron speed now uses the exact numbered tabletop ruler bands: Speed N
  reaches Distance N, including the ruler's non-linear Distance 2-5 marks.
- Ship overlap follows the tabletop maneuver procedure: ships may pass through
  one another, but an overlapping endpoint retries the same course one speed
  lower until a legal endpoint is found without changing the speed dial.
- Speed-0 ships may yaw in place without collision damage at half the ram yaw
  allowance.
- Huge-base firing arcs originate at the base center while all range bands
  measure from the selected hull-zone edge and ignore out-of-arc defender
  geometry.
- Accuracy results can lock every defense-token type the defender possesses,
  including exhausted or currently unusable tokens.
- Skilled First Officer command discard/reveal flow, Seventh Fleet damage
  choices, and same-player squadron re-selection no longer dead-end or add
  unnecessary pass-through clicks.

### Presentation, controls, and UI

- Dossiers use real defense-token symbols, show ship weight class, and wrap or
  autosize long ship names within the panel.
- Selected multi-choice dice, defense, and critical options use a persistent
  glowing-blue interior; critical choices also provide a Back button before
  committing.
- Objective panels, notifications, tooltips, and spatial callouts received
  clipping, lifetime, page-scope, and interaction fixes.
- Waiting-player UI is fully opaque and frontmost while still allowing public
  ship condition and weapon inspection where appropriate.
- Normal and Shift-WASD tactical-camera panning are 230% of their previous base
  speed.
- Activated-unit rings, battlefield contrast, UI audio behavior, firing-range
  holograms, Intel carrier placement, and objective-card presentation were
  refined for readability.

### Download

#### Windows x64

Download `SWArmada-0.1.2-Windows-x64.zip`, extract the complete archive, and
run `SWArmada.exe`.

SHA-256:
`605303C2D28A4C5A5A768D7E546BD503DD494B9FE9120AA6B6D3B472028DB782`

#### Linux x86-64

Download `SWArmada-0.1.2-Linux-x86_64.tar.gz`, extract the complete archive,
and run `./SWArmada.x86_64`. If necessary, restore its executable permission
with `chmod +x SWArmada.x86_64`.

SHA-256:
`8014EB09A9246C709185BD494137BD1C1B625D0E67CC71F469F4F73A31F34E37`

## [0.1.1](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.1) - 2026-08-01

Version 0.1.1 makes it much easier to find another commander and start an
online match.

### Worldwide player list

- Added an opt-in player list to the right side of the main menu.
- Players choose their own username and receive an automatic, stable
  `#NNNN` identifier.
- No Unity account, password, or account setup is required; authentication is
  anonymous and cached locally.
- Online and in-match states update through Unity Multiplayer Services.
- Your chosen name and anonymous identity persist across game updates on the
  same computer.

### Direct match invitations

- Available players can be invited directly from the worldwide player list.
- Sending an invitation creates the same private Relay-backed lobby used by
  the existing host/join-code flow.
- Accepting an invitation joins that lobby without manually copying a code.
- Player handles now carry into the online lobby and chat.
- Manual hosting and join codes continue to work normally.

### Update notifications

- The game now checks the latest GitHub Release once during startup.
- When a newer semantic version is available, an in-game notification shows
  the installed and available versions.
- The notification includes a button that opens the release page on GitHub.
- A failed or unavailable update check never blocks the game from starting.

### Download

#### Windows x64

Download `SWArmada-0.1.1-Windows-x64.zip`, extract the entire archive, and run
`SWArmada.exe`.

`1235AE580266B03EFDAADC51A7F3DB4E67209DCD4FA5DA406F4ACD20BE771306`

#### Linux x86-64

Download `SWArmada-0.1.1-Linux-x86_64.tar.gz`, extract the entire archive, and
run `./SWArmada.x86_64`. If needed, restore the executable permission with
`chmod +x SWArmada.x86_64`.

`CE63BA7203B117E72033D9555E6CCEB4B303F56F78560AB67D4A4DAC085AC5AC`

## [0.1.0](https://github.com/thetrufflegouda/SWArmada/releases/tag/v0.1.0) - 2026-08-01

First public baseline release of SWArmada for Windows x64.

Download the ZIP, extract the entire archive to a writable folder, and run `SWArmada.exe`.

**SHA-256**
`F9A2E9E2201B35FE8EBBEE4EB9C7CCFF6E2F8EF132EDB527710DDD006834A6A8`
