# PyPassGen - Python Password Generator

![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

A simple, secure Python password generator that creates cryptographically strong passwords for your security needs.

## 🚀 Quick Start

Clone the repository:
```bash
git clone https://github.com/pbssubhash/PyPassGen.git
```

Navigate to directory:
```bash
cd PyPassGen
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Run the generator:
```bash
python Example.py
```

## 📋 Table of Contents

- [Installation](#-installation)
- [Usage](#-usage)
- [How It Works](#-how-it-works)
- [Project Structure](#-project-structure)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)

## 💻 Installation

### Prerequisites

- Python 3.6 or higher
- No additional dependencies required

### Step 1: Install Python

#### 🖥️ Windows

**Option 1: Official Python Installer**
1. Go to [python.org/downloads](https://www.python.org/downloads/)
2. Download Python 3.6+ for Windows
3. Run installer and **check "Add Python to PATH"**
4. Verify installation:

<!-- Copy: python --version -->
```cmd
python --version
```

**Option 2: Microsoft Store**
Search "Python" in Microsoft Store and install

**Option 3: Package Manager**
Using Chocolatey:
<!-- Copy: choco install python -->
```cmd
choco install python
```

Using Scoop:
<!-- Copy: scoop install python -->
```cmd
scoop install python
```

#### 🍎 macOS

**Option 1: Homebrew (Recommended)**
Install Homebrew if not installed:
<!-- Copy: /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" -->
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install Python:
<!-- Copy: brew install python -->
```bash
brew install python
```

Verify installation:
<!-- Copy: python3 --version -->
```bash
python3 --version
```

**Option 2: Official Installer**
1. Go to [python.org/downloads/macos](https://www.python.org/downloads/macos/)
2. Download and install Python 3.6+
3. Verify installation:
<!-- Copy: python3 --version -->
```bash
python3 --version
```

#### 🐧 Linux

**Ubuntu/Debian:**
Update package list:
<!-- Copy: sudo apt update -->
```bash
sudo apt update
```

Install Python:
<!-- Copy: sudo apt install python3 python3-pip -->
```bash
sudo apt install python3 python3-pip
```

Verify installation:
<!-- Copy: python3 --version -->
```bash
python3 --version
```

**RHEL/CentOS/Fedora:**
RHEL/CentOS:
<!-- Copy: sudo dnf install python3 python3-pip -->
```bash
sudo dnf install python3 python3-pip
```

Fedora:
<!-- Copy: sudo dnf install python3 python3-pip -->
```bash
sudo dnf install python3 python3-pip
```

Verify installation:
<!-- Copy: python3 --version -->
```bash
python3 --version
```

**Arch Linux:**
Install Python:
<!-- Copy: sudo pacman -S python python-pip -->
```bash
sudo pacman -S python python-pip
```

Verify installation:
<!-- Copy: python --version -->
```bash
python --version
```

### Step 2: Download PyPassGen

**Method 1: Git Clone (Recommended)**
```bash
git clone https://github.com/pbssubhash/PyPassGen.git
```

Navigate to directory:
```bash
cd PyPassGen
```

**Method 2: Download ZIP**
1. Go to [github.com/pbssubhash/PyPassGen](https://github.com/pbssubhash/PyPassGen)
2. Click "Code" → "Download ZIP"
3. Extract the ZIP file
4. Navigate to the extracted folder

### Step 3: Verify Installation

Check if file exists:
```bash
ls PyPassGen.py
```

Test run:
```bash
python PyPassGen.py
```

## 🔧 Usage

### Basic Usage

Run the password generator:
```bash
python Example.py
```

**On macOS/Linux, you might need:**
```bash
python3 Example.py
```

### Interactive Session

```
$ python Example.py
Enter the number of characters you want in the password: 16
Generated Password: K8#mN2$vR9@pL3!x
```

### Common Password Lengths

| Length | Use Case | Command |
|--------|----------|---------|
| 8-12   | Basic accounts | Enter `12` when prompted |
| 16-20  | Important accounts | Enter `16` when prompted |
| 24-32  | High-security accounts | Enter `24` when prompted |

### Platform-Specific Commands

#### 🖥️ Windows Commands

Command Prompt:
```cmd
python Example.py
```

PowerShell:
```powershell
python Example.py
```

If python command not found, try:
```cmd
py Example.py
```

```cmd
py -3 Example.py
```

#### 🍎 macOS Commands

Terminal:
```bash
python3 Example.py
```

If you have Python 3 as default:
```bash
python Example.py
```

Make executable (optional):
```bash
chmod +x Example.py
```

```bash
./Example.py
```

#### 🐧 Linux Commands

Most distributions:
```bash
python3 Example.py
```

Arch Linux (Python 3 is default):
```bash
python Example.py
```

Make executable:
```bash
chmod +x Example.py
```

```bash
./Example.py
```

## 🔍 How It Works

PyPassGen uses Python's built-in `secrets` module to generate cryptographically secure passwords, with `pyperclip` for clipboard functionality.

### Dependencies

- **secrets** (built-in) - Cryptographically secure random number generation
- **string** (built-in) - Character set definitions
- **pyperclip** - Cross-platform clipboard access for easy password copying

### Character Set

The generator uses these character types:
- **Uppercase letters**: A-Z (26 characters)
- **Lowercase letters**: a-z (26 characters)
- **Numbers**: 0-9 (10 characters)
- **Special characters**: !@#$%^&*()_+-= (13+ characters)

### Security Features

✅ **Cryptographically secure** - Uses `secrets.choice()` for random generation  
✅ **No predictable patterns** - Each character is independently selected  
✅ **Offline generation** - No internet connection required  
✅ **No data storage** - Passwords are not saved or logged  
✅ **Clipboard integration** - Easy copying with pyperclip

### Password Strength

| Length | Combinations | Estimated Crack Time |
|--------|-------------|---------------------|
| 8      | 2.7 × 10¹⁵  | Hours to days      |
| 12     | 4.8 × 10²³  | Years              |
| 16     | 8.6 × 10³¹  | Thousands of years |
| 24     | 2.7 × 10⁴⁸  | Millions of years  |

## 📁 Project Structure

```
PyPassGen/
├── Example.py            # Main password generator script
├── README.md             # This documentation
├── LICENSE               # MIT License
└── requirements.txt      # Python dependencies (pyperclip)
```

### Code Structure

```python
# Example.py structure
import secrets            # Cryptographically secure random
import string            # Character set definitions
import pyperclip         # Clipboard functionality

def generate_password(length):
    # Character set definition
    characters = string.ascii_letters + string.digits + "!@#$%^&*()_+-="
    
    # Generate password
    password = ''.join(secrets.choice(characters) for _ in range(length))
    return password

# Main execution
if __name__ == "__main__":
    # Get user input
    # Generate password
    # Copy to clipboard (pyperclip)
    # Display result
```

## 🛠️ Troubleshooting

### Common Issues

#### ❌ "python: command not found"

**On Windows:**
Try these alternatives:
```cmd
py Example.py
```

```cmd
py -3 Example.py
```

```cmd
python3 Example.py
```

**On macOS/Linux:**
Try python3 instead:
```bash
python3 Example.py
```

Or install Python:
- macOS: 
```bash
brew install python
```
- Ubuntu: 
```bash
sudo apt install python3
```

#### ❌ "No such file or directory"

Check you're in the right directory:
```bash
pwd
```

```bash
ls -la
```

Navigate to PyPassGen directory:
```bash
cd PyPassGen
```

Verify file exists:
```bash
ls Example.py
```

#### ❌ "Permission denied"

**On Windows:**
Run as Administrator or use:
```cmd
python Example.py
```

**On macOS/Linux:**
Make executable:
```bash
chmod +x Example.py
```

Or run with python:
```bash
python3 Example.py
```

#### ❌ "ModuleNotFoundError: No module named 'pyperclip'"

Install the required dependencies:
```bash
pip install -r requirements.txt
```

Or install pyperclip directly:
```bash
pip install pyperclip
```

On macOS/Linux, you might need:
```bash
pip3 install pyperclip
```

#### ❌ "ModuleNotFoundError" (other modules)

Check Python version:
```bash
python --version
```

Should be Python 3.6 or higher
If not, upgrade Python

#### ❌ Program hangs or doesn't respond

Press Ctrl+C to stop the program
Then run again:
```bash
python Example.py
```

Make sure to enter a number when prompted

### Getting Help

- **Issues**: [GitHub Issues](https://github.com/pbssubhash/PyPassGen/issues)
- **Questions**: Create a new issue with "Question" label
- **Documentation**: Check this README first

## 🤝 Contributing

### Quick Contribution Guide

1. **Fork** the repository
2. **Clone** your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/PyPassGen.git
   ```
3. **Create** a branch:
   ```bash
   git checkout -b feature/your-feature
   ```
4. **Make** your changes
5. **Test** your changes:
   ```bash
   python Example.py
   ```
6. **Commit** and **push**:
   ```bash
   git add .
   ```
   ```bash
   git commit -m "Add your feature"
   ```
   ```bash
   git push origin feature/your-feature
   ```
7. **Create** a Pull Request

### Development Setup

Clone the repository:
```bash
git clone https://github.com/pbssubhash/PyPassGen.git
```

```bash
cd PyPassGen
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Test the application:
```bash
python Example.py
```

Ready to contribute!

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **pbssubhash** - Original creator
- **Python Software Foundation** - For the `secrets` module
- **Contributors** - Everyone who helps improve this project

---

**Made with ❤️ for better password security**

*Last updated: 2024-07-09*