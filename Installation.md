# Installation Steps

## Step 1: Download the Installer

1. Open your web browser and go to the official Python website: [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. The site automatically detects your operating system and displays a recommended download button. Click it to download the latest stable version.
3. Alternatively, browse to the **Downloads** section for a specific operating system (Windows, macOS, or Linux/Source) to choose a specific version.

## Step 2: Run the Installer

### Windows
1. Double-click the downloaded `.exe` file.
2. **Important:** Check the box labeled **"Add python.exe to PATH"** at the bottom of the installer window before proceeding. This step is often missed and is the most common cause of installation problems.
3. Click **Install Now** for the default installation, or **Customize Installation** to choose a specific install location and optional features.
4. Wait for the installation to complete, then click **Close**.

### macOS
1. Double-click the downloaded `.pkg` file.
2. Follow the on-screen instructions in the installation wizard, agreeing to the license terms.
3. Enter your administrator password if prompted.
4. Click **Install** and wait for the process to finish.

### Linux
Many Linux distributions include Python 3. If it is missing, use your distribution's package manager. These commands apply to the listed distributions; consult your distribution's documentation for others.

```bash
# Debian/Ubuntu
sudo apt update
sudo apt install python3 python3-pip

# Fedora
sudo dnf install python3 python3-pip

# Arch
sudo pacman -S python python-pip
```

## Step 3: Confirm Installation Location (Optional)

- **Windows:** By default, Python installs to `C:\Users\<YourUsername>\AppData\Local\Programs\Python\`
- **macOS:** By default, Python installs to `/Library/Frameworks/Python.framework/` or via `/usr/local/bin/python3`
- **Linux:** Typically installed to `/usr/bin/python3`

---

# Verification Steps

After installation, confirm that Python was installed correctly.

## Step 1: Open a Terminal or Command Prompt

- **Windows:** Press `Win + R`, type `cmd`, and press Enter (or search for "Command Prompt" / "PowerShell")
- **macOS:** Open **Terminal** from Applications > Utilities, or search via Spotlight
- **Linux:** Open your distribution's terminal application

## Step 2: Check the Python Version

Use the command for your operating system:

```bash
# Windows
py --version

# macOS and Linux
python3 --version
```

On Windows, `python --version` may also work if Python was added to `PATH`. The output should show a Python 3 version, for example:

```bash
Python 3.x.x
```

## Step 3: Check that pip Is Installed

Run pip through the same Python interpreter to avoid using a different installation by mistake:

```bash
# Windows
py -m pip --version

# macOS and Linux
python3 -m pip --version
```

## Step 4: Run a Test Script

1. Start the Python interactive shell with `py` on Windows or `python3` on macOS and Linux.
2. At the `>>>` prompt, enter:

```python
print("Python installed successfully!")
```

3. If the message prints without errors, your installation is working correctly.
4. Type `exit()` to leave the interactive shell.

---

# Troubleshooting

| Problem | Likely Cause | Solution |
|---------|--------------|----------|
| `'python' is not recognized` (Windows) | Python is not on `PATH`, or the Windows launcher is being used instead | Try `py --version`. If that works, use `py` to run Python. Otherwise, rerun the installer and enable the option to add Python to `PATH`. |
| `command not found: python` (macOS/Linux) | The system uses the `python3` command | Use `python3` and `python3 -m pip` rather than creating a system-wide alias. |
| `No module named pip` | pip is not installed for the selected interpreter | Try `py -m ensurepip --upgrade` on Windows or `python3 -m ensurepip --upgrade` on macOS/Linux. If unavailable, follow the package manager instructions for your OS. |
| Permission denied while installing a package | The selected environment is not writable | Use a virtual environment for project packages instead of changing system Python permissions. See the [Python venv guide](https://docs.python.org/3/library/venv.html). |
| Multiple Python versions causing conflicts | Older version(s) already installed | Use a version manager such as `pyenv`, or explicitly call the correct version (e.g., `python3.12`) |
| Installer fails or freezes | Incomplete download or an installer-specific issue | Download a fresh installer from [python.org](https://www.python.org/downloads/) and check the error message before changing antivirus or firewall settings. |
| SSL certificate errors when using pip | Certificate or network configuration issue | Confirm the system date and network/proxy settings, then consult your organization's support or the [pip user guide](https://pip.pypa.io/en/stable/user_guide/). |

Avoid uninstalling the Python version supplied by Linux distributions, because system tools may depend on it. If a problem persists, consult the [official Python documentation](https://docs.python.org/3/using/index.html) or your operating system's support resources.
