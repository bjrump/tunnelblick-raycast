# Tunnelblick Toggle for Raycast

This Raycast extension allows you to quickly connect and disconnect your Tunnelblick VPN configurations directly from Raycast.

## Features

- **Smart Toggling**: Automatically detects your available VPN configuration.
- **Single or Multiple Configs**: Works seamlessly whether you have one or multiple VPN profiles.
- **Status Feedback**: Displays HUD notifications for "Connecting..." and "Disconnecting...".
- **Zero Configuration**: No complex setup required—it just reads from Tunnelblick.

## How it Works

The extension uses AppleScript to communicate with the Tunnelblick application. It:
1.  Retrieves the list of available configurations.
2.  Identifies the first valid configuration name.
3.  Checks its current state (Connected/Disconnected).
4.  Toggles it accordingly.

## Installation

1.  Clone this repository.
2.  Run `npm install`.
3.  Run `npm run dev` to start the development server.
4.  Open Raycast and search for "Toggle VPN".

## Requirements

- **Tunnelblick** (running)
- **Raycast**
- **Permissions**: You must allow Raycast to control Tunnelblick via AppleScript (macOS will prompt you on first run).

## License

MIT
