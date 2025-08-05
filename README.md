# 🧠 Face Recognition Setup Guide (Windows)

This guide walks you through setting up a Python virtual environment and installing the `face_recognition` library properly on a Windows system.

---

## 📌 Requirements

- Windows 10/11 (64-bit)
- Python 3.6 to 3.10 (⚠️ **Not compatible with Python 3.12+**)
- Internet connection
- Admin rights (for installing system packages)

---

## ✅ Step 1: Install Compatible Python Version (if needed)

### 🔹 Check your current Python version:
```bash
python --version
```
```If it’s Python 3.11 or higher, download Python 3.10 or 3.9 from:
https://www.python.org/downloads/
```
🔸 During installation, make sure to:
- ✅ Check “Add Python to PATH”
- ✅ Enable pip
- ✅ Enable virtualenv (optional)

## ✅ Step 2: Create a Virtual Environment
1. Open Command Prompt and go to your project directory:
```
cd path\to\your\project
```
2. Create a virtual environment:
```
python3.10 -m venv venv      #python(VersionName) -m venv FolderName
```
3. Activate the virtual environment:
```
venv\Scripts\activate
```
🔹 Your prompt will change to show (venv) — you're now inside the virtual environment.

## ✅ Step 3: Install Build Tools (One-Time Setup)
🔹 Install Visual C++ Build Tools:
- Go to:
```
 https://visualstudio.microsoft.com/visual-cpp-build-tools/
```
During installation, select:
- ✅ C++ build tools
- ✅ Windows 10 SDK
- ✅ CMake tools for Windows
These are required to build dlib, a dependency of face_recognition.

## ✅ Step 4: Install CMake (if not installed)
🔹 Download from:
- Go to:
```
https://cmake.org/download/
```
- Install and make sure CMake is added to PATH during installation.
- Confirm CMake installation:
```
cmake --version
```

## ✅ Step 5: Install dlib (core dependency)
Option 1: Install via pip (works with Python 3.6–3.10)
```
pip install dlib==19.24.2
```
Option 2: (If pip install fails) Install from .whl
1. Download prebuilt .whl for your Python version from:
```
https://www.lfd.uci.edu/~gohlke/pythonlibs/#dlib
```
Example install:
```
pip install dlib‑19.24.2‑cp310‑cp310‑win_amd64.whl
```

## ✅ Step 6: Install face_recognition
After successful dlib installation, run:
```
pip install face_recognition
```

## ✅ Step 7: Verify Installation
```
python -c "import face_recognition; print(face_recognition.__version__)"
```
You should see a version number like 1.3.0.

## ✅ Optional: Install Additional Tools
```
pip install opencv-python numpy
```

## 🧹 Resetting the Environment (if needed)
If something breaks, simply delete the venv folder and redo from Step 2.

## ✅ Final Notes
- Always activate venv before running your face recognition scripts.
- This setup avoids most installation issues by keeping everything isolated.











