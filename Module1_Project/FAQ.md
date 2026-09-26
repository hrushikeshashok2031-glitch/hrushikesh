# Frequently Asked Questions

**Q1: Which version of Python should I install?**
A: Install the latest stable Python 3 release available on [python.org](https://www.python.org/downloads/). Avoid Python 2, as it is no longer supported or maintained.

**Q2: Do I need to install both Python and pip separately?**
A: Official Python installers generally include `pip`. Some Linux distributions package it separately, so install it with your distribution's package manager if needed. Check with `py -m pip --version` on Windows or `python3 -m pip --version` on macOS/Linux.

**Q3: Can I install multiple versions of Python on the same computer?**
A: Yes. Multiple versions can coexist. Tools like `pyenv` (macOS/Linux) or the Python Launcher (`py`, on Windows) make it easier to manage and switch between versions.

**Q4: What is the difference between `python` and `python3` commands?**
A: On many Linux and macOS systems, `python` may point to Python 2 (or may not exist at all), while `python3` explicitly refers to Python 3. Windows installations typically register `python` for Python 3 by default.

**Q5: Do I need administrator/root access to install Python?**
A: A system-wide installation may require administrator or root access. You can choose a per-user installer where available. For installing packages, use a virtual environment so project dependencies do not modify system Python.

**Q6: How do I uninstall Python if I need to reinstall it?**
A: The steps depend on how Python was installed:
- **Windows:** Use "Add or Remove Programs" in Settings
- **macOS:** Delete the Python framework folder or use a package manager like Homebrew if that was used to install it
- **Linux:** Avoid removing the Python version supplied by the distribution because system tools may depend on it. For Python installed separately, follow the instructions for the installer or package manager that was used.

**Q7: How do I install additional Python packages/libraries?**
A: Use `pip`, Python's package manager:

```bash
# Windows
py -m pip install <package-name>

# macOS and Linux
python3 -m pip install <package-name>
```

For project work, activate a virtual environment before installing packages.

**Q8: Is it necessary to add Python to the system PATH?**
A: It is convenient but not always necessary. On Windows, the Python launcher command `py` can work without manually adding `python.exe` to `PATH`. On macOS and Linux, use `python3` when `python` is unavailable.

**Q9: What should I use to write and run Python code after installation?**
A: Any text editor works, but dedicated code editors such as Visual Studio Code, PyCharm, or Jupyter Notebook provide helpful features like syntax highlighting, debugging, and code completion.

---

# Conclusion

Installing Python is a straightforward process once the software requirements are met and the correct installation steps are followed for your operating system. By downloading the official installer, ensuring Python is added to the system PATH, and verifying the installation through the terminal, you can confirm that your environment is ready for development.

This documentation covered the essential steps: understanding what Python is, checking system requirements, installing Python correctly, verifying the installation, and resolving common issues. With Python successfully installed, you are now ready to begin writing and running Python programs, and to explore its extensive ecosystem of libraries and frameworks for tasks ranging from simple scripting to advanced data science and web development.

For further learning, refer to the [official Python documentation](https://docs.python.org/3/) and the [Python tutorial](https://docs.python.org/3/tutorial/index.html) for beginners.
