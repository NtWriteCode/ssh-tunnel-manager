# SSH Tunnel Manager GUI

[![Build status](https://github.com/NtWriteCode/ssh-tunnel-manager/actions/workflows/main-build.yml/badge.svg)](https://github.com/NtWriteCode/ssh-tunnel-manager/actions/workflows/main-build.yml)

A modern, user-friendly desktop application for managing SSH tunnels with ease.

## Overview

The SSH Tunnel Manager simplifies creating, managing, and executing SSH tunnels through an intuitive Graphical User Interface (GUI). Built with Python and PyQt6, it allows for easy configuration of connection profiles, port forwarding, and tunnel control.

## Key Features

*   **Intuitive Profile Management:** Save, load, and manage multiple SSH connection profiles (server, port, key, port mappings).
*   **Easy Port Forwarding:** Configure multiple local-to-remote port mappings per profile.
*   **Simple Tunnel Control:** Start/stop tunnels with a click. Copy the underlying SSH command if needed.
*   **Real-time Status:** Clear visual feedback on tunnel status (Idle, Starting, Running, Stopped, Errors).
*   **Automatic Persistence:** Profiles are saved to `~/.config/ssh_tunnel_manager/config.json`.
*   **User-Friendly Design:** Dynamic UI adjustments and clear visual cues for an improved experience.

## Requirements (for running from source)

*   Python 3.x
*   PyQt6 (`PyQt6>=6.0.0`)
*   `typing-extensions>=4.0.0`
*   An SSH client installed and available in your system's PATH (e.g., OpenSSH).

## Getting Started

### Using a Release (Recommended)

1.  Go to the [Releases page](https://github.com/NtWriteCode/ssh-tunnel-manager/releases).
2.  Download the latest executable for your operating system (Windows, macOS, or Linux).
3.  Run the downloaded application. No installation is typically required.

### Running from Source (for Development)

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/NtWriteCode/ssh-tunnel-manager.git
    cd ssh-tunnel-manager
    ```
2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\\Scripts\\activate
    ```
3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the application:**
    ```bash
    python main.py
    ```

## Configuration

Once the application is running:

*   **Server:** Enter the SSH server address (`user@hostname`).
*   **SSH Port:** Specify the SSH server port (defaults to 22).
*   **SSH Key File:** (Optional) Path to your SSH private key (tilde `~` expansion supported).
*   **Port Forwarding:** Add/remove `Local Port` to `Remote Port` mappings.
*   **Profiles:** Save, load, or delete configurations. Changes are auto-saved.
*   **Controls:** Use "Start/Stop Tunnel" and "Copy SSH Command" as needed.

Application data is stored in `~/.config/ssh_tunnel_manager/config.json`.

## Building from Source

The project uses PyInstaller. The GitHub Actions workflow (`.github/workflows/main-build.yml`) handles release builds.

To build manually:
1.  Install build dependencies: `pip install pyinstaller`
2.  Navigate to the project root.
3.  Run PyInstaller: `pyinstaller --onefile --name ssh-tunnel-manager main.py`
    (Add `--windowed` for a no-console build on Windows).
    Executables are found in the `dist` directory.

## Contributing

Contributions are welcome! Please fork the repository, create a feature branch, commit your changes, and open a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m \'Add some AmazingFeature\'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.
