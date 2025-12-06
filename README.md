ESP + Fly LocalScript (Roblox)

Client-side ESP and fly controls. Highlights other players using Highlight , displays username and distance below their character, and provides a smooth fly toggle with basic jitter to avoid perfectly constant motion. Streaming-safe: reliably attaches to players as they join, die/respawn, and leave.

Features
- ESP highlights all other players and shows USERNAME [Xm] below the character.
- Streaming-aware: rebinds the label Adornee when parts load; handles respawns and leaves.
- Toggle ESP on/off with status prints to the console.
- 500m visibility cutoff to reduce clutter.
- Fly mode with jittered velocity to look natural to an ac; camera-forward lock.

Keybinds
- Y : Toggle fly mode
- U : Toggle ESP (highlight + username/distance)
- Console prints show “ESP ENABLED” or “ESP IS DISABLED” on load and toggles.
Placement

- Script type: LocalScript
- Location: StarterPlayerScripts
- Dependencies: Players , RunService , UserInputService , workspace.CurrentCamera.

How It Works
- Tracks lifecycle events: PlayerAdded , PlayerRemoving , CharacterAdded , CharacterRemoving .
- Creates a randomized Folder container, Highlight , and BillboardGui per player.
- Continuously updates username/distance and visibility based on range and toggle state.
- Rebinds the BillboardGui.Adornee when HumanoidRootPart / Head becomes available to handle streamed characters.
Configuration

- MAX_VIS_DISTANCE : 500
- Label offset: BillboardGui.StudsOffsetWorldSpace = Vector3.new(0, -6, 0).
- Fly speed: baseSpeed = 100.

Loadstring:
- loadstring(game:HttpGet("https://raw.githubusercontent.com/CaughtByAmaze/ESP-Fly-LocalScript-Roblox/refs/heads/main/amaze.lua"))() 
