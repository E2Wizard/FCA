## CCcam Configuration Script

This script automates the process of fetching, filtering, and updating CCcam server configurations from various sources.
It collects free CCcam server details from multiple URLs, processes them, and updates the local cam configuration file.


## Description

The script performs the following tasks:

1. **Create Directory**: It checks and creates a temporary directory `/tmp/xtest`.
2. **Download and Extract CCcam Server Details**: It uses `curl` to download CCcam server details from several predefined URLs. It then processes these details using `grep`, `sed`, and `awk` to extract relevant information such as address, port, username, and password.
3. **Compile and Clean Up**: It compiles the extracted server details, removes unnecessary entries, and updates the CCcam configuration file (`/etc/CCcam.cfg`). It also generates configuration files for different applications (like OSCam).


## Usage

1. **Ensure Script Permissions**: Make sure the script has executable permissions.
   ```bash
   chmod +x script.sh
