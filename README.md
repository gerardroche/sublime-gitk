# Gitk

Enhance your Sublime Text experience with seamless [`gitk`](https://git-scm.com/docs/gitk/) integration.

Provides commands to launch `gitk` from within Sublime Text.

## Installation

### Step 1: Install `gitk`

Before you get started, make sure you have [`gitk`](https://git-scm.com/docs/gitk/) installed on your system. To install, you'll need to follow the instructions specific to your operating system:

**On Windows:**

1. Download the Git for Windows installer from the official website: [Git for Windows](https://gitforwindows.org/).

2. Run the installer and follow the installation steps. During installation, you can choose the components to install. Ensure that the "Git Bash Here," "Git GUI Here," and "Gitk" options are selected.

3. Complete the installation, and Gitk will be installed along with Git on your Windows system.

**On macOS:**

1. You can install Gitk on macOS using a package manager like Homebrew. If you don't have Homebrew installed, you can install it by following the instructions on the Homebrew website: [Homebrew](https://brew.sh/).

2. Once Homebrew is installed, open your terminal and run the following command to install Gitk:

   ```bash
   brew install gitk
   ```

3. Homebrew will download and install Gitk and its dependencies.

**On Linux (Ubuntu/Debian):**

1. Open a terminal.

2. Use the package manager to install Gitk. For Ubuntu and Debian-based systems, you can use `apt-get`:

   ```bash
   sudo apt-get update
   sudo apt-get install gitk
   ```

**On Linux (Fedora/RHEL/CentOS):**

1. Open a terminal.

2. Use the package manager to install Gitk. For Fedora, RHEL, or CentOS-based systems, you can use `dnf` or `yum`:

   For Fedora:

   ```bash
   sudo dnf install gitk
   ```

   For RHEL/CentOS:

   ```bash
   sudo yum install gitk
   ```

After following these steps, Gitk should be successfully installed on your system. You can verify the installation by opening a terminal and running the following command:

```bash
gitk --version
```

This command should display the version information of Gitk, confirming that it's installed and ready to use.

### Step 2: Install the Gitk Package

**Pending availability https://github.com/wbond/package_control_channel/pull/8818**

**Method 1: Using Package Control**

1. Open Sublime Text.
2. Access the Command Palette by pressing `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS).
3. Type "Package Control: Install Package" and press `Enter`.
4. In the input field, type "Gitk" and select it from the list of available packages.

**Method 2: Manual Installation**

1. Visit the [Gitk GitHub repository](https://github.com/gerardroche/sublime-gitk).
2. Click on the "Code" button and choose "Download ZIP."
3. Unzip the downloaded file.
4. In Sublime Text, navigate to `Preferences -> Browse Packages...` to access the Packages folder.
5. Copy the "Gitk" folder from the unzipped archive and paste it into the Packages folder.

**Method 3: Manual Git Repository Installation**

1. Open a terminal or command prompt.
2. Go to the Sublime Text Packages directory based on your operating system:
   - Windows: `%APPDATA%\Sublime Text\Packages`
   - macOS: `~/Library/Application Support/Sublime Text/Packages`
   - Linux: `~/.config/sublime-text/Packages`
3. Clone the Gitk plugin repository directly into the Packages directory using Git:

   ```bash
   git clone https://github.com/gerardroche/sublime-gitk.git Gitk
   ```

## Commands

Use these commands to launch `gitk`.

Command                     | Description
:---------------------------| :----------
**Gitk**                    | Launch `gitk` for the current repository.
**Gitk&nbsp;--all**         | Open `gitk --all` for the current repository.

## NeoVintageous mappings

[NeoVintageous](https://github.com/NeoVintageous/NeoVintageous) is a Vim emulator for Sublime Text.

1. Open the Command Palette: `Command Palette → NeoVintageous: Open neovintageous file`.

2. Add your preferred mappings.

   **Example**

   ```vim
   nnoremap <leader>oa :Gitk all=true<CR>
   nnoremap <leader>ok :Gitk max-count=200 all=true date-order=true<CR>
   ```

3. To apply the changes, reload the neovintageousrc from the Command Palette: `Command Palette → NeoVintageous: Reload neovintageous file`.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

Released under the [GPL-3.0-or-later License](LICENSE).
