# Agents & Architecture

This project follows a simple, agent-friendly architecture designed to be easily maintained and understood by both humans and AI agents.

## Project Structure

- **src/**: Contains the source code for the Raycast commands.
  - `toggle-vpn.ts`: The main logic for toggling the VPN connection.
- **assets/**: Stores icons and other static assets.
- **package.json**: Defines dependencies and scripts.

## Key Decisions

1.  **AppleScript Integration**: We use `run-applescript` to interface with Tunnelblick. This is necessary because Tunnelblick does not have a native CLI or API that is easily accessible from Node.js/Raycast environment.
2.  **Robust String Parsing**: Instead of relying on fragile AppleScript object iteration (which caused "Invalid key form" errors), we fetch the raw configuration string and parse it in TypeScript. This provides a more stable way to identify the target VPN configuration.
3.  **Zero-Config Philosophy**: The script automatically picks the first available configuration. This avoids the need for users to manually input their VPN name.

## Future Improvements

- Support for selecting a specific VPN if multiple are available (currently defaults to the first one).
- More detailed error handling for AppleScript failures.
