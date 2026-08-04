# SWArmada 0.1.2

Version 0.1.2 is the objective-gameplay release. It adds three complete custom
scenarios, expands fleet and map setup, introduces fleet-text importing and
persistent direct comms, and includes a broad rules, multiplayer, presentation,
and usability pass.

Republic and Separatist factions are intentionally deferred to version 0.1.3.

## New objective game modes

### Escort the VIP

- Playable long-approach objective with host-selectable Escort and Interceptor
  roles in online lobbies and the same P1/P2 choice in local hotseat.
- The Escort receives a faction-specific zero-point VIP Transport with its own
  shared combat profile, command behavior, deployment position, and objective
  HUD.
- The Escort wins by surviving to extract the VIP at the end of a round or by
  destroying every Interceptor capital ship. The Interceptor wins by destroying
  the VIP or preventing extraction through Round 10.
- VIP extraction requires the transport's full base inside the Extraction Zone.

### Seize the Station

- Playable center-station objective with explicit capture-or-continue choices,
  speed-0 capture, contesting, departure handling, and a full-round scoring
  delay.
- Uses the converted Metal station model and its original material groups as a
  static center objective.

### Intel Retrieval

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

## Scenario and map setup

- Custom maps now store a scenario assignment: Default, Escort the VIP, Seize
  the Station, or Intel Retrieval.
- Fleet Sandbox, local hotseat, and online setup offer maps appropriate to the
  selected scenario.
- Setup screens use a three-column fleet/scenario/fleet layout with objective
  cards shown at their native aspect ratio and a centered hover zoom.
- Escort the VIP and Intel Retrieval always use long-approach deployment.
- Objective matches keep both starting-area outlines visible throughout play.

## Fleet management and rules

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

## Online play, player directory, and comms

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

## Updating

- The startup update notice can automatically download the correct Windows ZIP
  or Linux tarball to the player's Downloads folder.
- Downloads use a unique partial file, verify the published SHA-256 sidecar,
  and promote only a valid archive. Failures remain readable and retryable
  without closing the game.

## Rules and combat improvements

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

## Presentation, controls, and UI

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

## Download

### Windows x64

Download `SWArmada-0.1.2-Windows-x64.zip`, extract the complete archive, and
run `SWArmada.exe`.

SHA-256:
`605303C2D28A4C5A5A768D7E546BD503DD494B9FE9120AA6B6D3B472028DB782`

### Linux x86-64

Download `SWArmada-0.1.2-Linux-x86_64.tar.gz`, extract the complete archive,
and run `./SWArmada.x86_64`. If necessary, restore its executable permission
with `chmod +x SWArmada.x86_64`.

SHA-256:
`8014EB09A9246C709185BD494137BD1C1B625D0E67CC71F469F4F73A31F34E37`
