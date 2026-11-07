# Pushpa — Was It Just a Dream? (3D story game)

All HTML, CSS and JavaScript are kept in one `index.html`.

## Story
The game follows the user's dream: phone call, surprise appearance, monkey teasing, lake crossing, lotus flowers, hand-holding, green meadow, family conversation, jealous friend, carrying scene, mountain sunrise, rose garden, heartbeat and waking up.

## Existing reference boards
Your supplied storyboards and garden image are in `assets/reference/`. They are visual references, not rigged 3D characters.

## Add realistic character models
Place rigged GLB models here:
- `assets/models/girl.glb` — female lead based on the supplied reference
- `assets/models/boy.glb` — male lead based on the supplied reference
- `assets/models/friend.glb` — optional friend character for the jealousy chapter

The game now attempts to load `girl.glb` and `boy.glb` automatically. If a model is missing, the 3D stand-in remains visible.

For the animation system, include animation clips in the GLB with these suggested names (case-insensitive):
- `Idle`
- `Walk`
- `Angry` (girl's annoyed / mock-angry reaction)
- `GiveFlowers` (boy)
- `Receive` (girl)
- `Hug`
- `Carry` (boy carrying girl)
- `Carried` (girl being carried)
- `Sit`
- `WakeUp`

The current integration automatically plays `Idle` and `Walk` when matching clips exist. Other clips are ready to be triggered in the story sequence in the next animation pass. Animation clip names must exist in the exported GLB; merely renaming a file does not create animations.

## Music
Add licensed audio files:
- `assets/audio/dream-piano.mp3`
- `assets/audio/lakeside-ambience.mp3`

Audio starts after the user presses "Enter the dream", as browsers block autoplay before interaction. Missing audio files do not stop the game.

## Upload
Upload the contents of this `game/` directory into your existing repository's `game/` directory. Keep any existing PNG character sprites if you want; the 3D model loader does not depend on them.
