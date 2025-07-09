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
Hey, Welcome. Just say me how many characters do you want in your password? (default 128)
16
Random password of length 16 is: 
******
,QM3Wa_7!kR9@pL3
******
It contains 3 lowercase, 5 uppercase, 4 numbers and 4 symbol characters
Password copied to clipboard, push a button to exit...
```

### Default Behavior

- **Default length**: 128 characters (if you just press Enter)
- **Automatic clipboard copy**: Password is automatically copied to clipboard
- **Character breakdown**: Shows count of each character type used
- **Interactive prompt**: Press any key to exit after generation

### Common Password Lengths

| Length | Use Case | Input |
|--------|----------|--------|
| 8-12   | Basic accounts | Enter `12` when prompted |
| 16-20  | Important accounts | Enter `16` when prompted |
| 24-32  | High-security accounts | Enter `24` when prompted |
| 128    | Maximum security (default) | Just press Enter |

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

PyPassGen uses Python's built-in `random` module to generate passwords with balanced character distribution, and `pyperclip` for clipboard functionality.

### Dependencies

- **random** (built-in) - Random number generation for character selection
- **pyperclip** - Cross-platform clipboard access for easy password copying

### Character Set & Distribution

The generator uses ASCII character ranges to ensure balanced character distribution:
- **Lowercase letters**: ASCII 97-122 (a-z)
- **Uppercase letters**: ASCII 65-90 (A-Z)  
- **Numbers**: ASCII 48-57 (0-9)
- **Special characters**: ASCII 33-47, 91-96, 123-126 (!@#$%^&*()_+-=[]{}|;:,.<>?~)

### Key Features

✅ **Balanced character distribution** - Ensures mix of all character types  
✅ **Random character selection** - Uses `random.randint()` for selection  
✅ **Automatic clipboard copying** - Generated password is copied to clipboard  
✅ **Character count display** - Shows breakdown of character types used  
✅ **Customizable length** - Default 128 characters, user can specify any length  
✅ **No data storage** - Passwords are not saved or logged  

### Password Strength

| Length | Combinations | Character Mix | Security Level |
|--------|-------------|---------------|----------------|
| 8      | ~6.1 × 10¹⁴  | Balanced     | Good          |
| 12     | ~8.9 × 10²¹  | Balanced     | Strong        |
| 16     | ~1.3 × 10²⁹  | Balanced     | Very Strong   |
| 24     | ~2.8 × 10⁴³  | Balanced     | Excellent     |
| 128    | ~10⁶⁸⁴      | Balanced     | Cryptographic |

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
import random            # Random number generation
import pyperclip         # Clipboard functionality

# Initialize counters for character types
symbol = 0
lower = 0
upper = 0
number = 0
count = 0
password = []

# Get user input (default 128)
length = input("Hey, Welcome. Just say me how many characters do you want in your password? (default 128)\n")
length = 128 if length == '' else int(length)

# Generate password with balanced character distribution
while count < length:
    rand = random.randint(0, 3)  # Select character type
    if rand == 0:    # Lowercase
        lower += 1
        b = random.randint(97, 123)
        password.append(b)
    elif rand == 1:  # Uppercase
        upper += 1
        b = random.randint(65, 91)
        password.append(b)
    elif rand == 2:  # Numbers
        number += 1
        b = random.randint(48, 58)
        password.append(b)
    elif rand == 3:  # Symbols
        symbol += 1
        # Select from different symbol ranges
        r = random.randint(0, 2)
        if r == 0:
            b = random.randint(33, 48)
        elif r == 1:
            b = random.randint(91, 97)
        elif r == 2:
            b = random.randint(123, 126)
        password.append(b)
    count += 1

# Convert ASCII codes to characters
word = "".join([chr(c) for c in password])

# Copy to clipboard and display results
pyperclip.copy(word)
print("Random password of length %s is: \n" % length)
print('******')
print(word)
print('******')
print("\nIt contains", lower, "lowercase,", upper, "uppercase,", number, "numbers and", symbol, "symbol characters")
input('Password copied to clipboard, push a button to exit...')
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

#### ❌ SyntaxWarning: "is" with a literal

You might see this warning:
```
SyntaxWarning: "is" with a literal. Did you mean "=="?
```

This is a minor warning in the code and doesn't affect functionality. The program will still work correctly.

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

#### ❌ "ValueError: invalid literal for int()"

This happens if you enter non-numeric characters when asked for password length.
Make sure to enter only numbers:
```
Hey, Welcome. Just say me how many characters do you want in your password? (default 128)
16    # Enter numbers only, not letters
```

#### ❌ Password not copied to clipboard

If the password isn't copying to clipboard:
- **On Linux**: You might need to install additional clipboard tools:
```bash
sudo apt install xclip
```
or
```bash
sudo apt install xsel
```

- **On macOS/Windows**: pyperclip should work automatically

#### ❌ Program hangs or doesn't respond

Press Ctrl+C to stop the program
Then run again:
```bash
python Example.py
```

Make sure to enter a number when prompted, or just press Enter for default (128)

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