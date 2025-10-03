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
```
python --version
```

- To download Python 3.10 Go to the official Python download page:

```
https://www.python.org/downloads/release/python-3100/
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
py -3.10 -m venv venv    # (venv) folder name or rename it as you want
```
3. Activate the virtual environment:
```
venv\Scripts\activate        #  FolderName\Scripts\Activate
```
🔹 Your prompt will change to show (venv) — you're now inside the virtual environment.[Example image](assets/venv_creating.jpg)

### NOTE 
this virtual environment work well on different IDEs.[How](assets/venv_work_on.png)

## ✅ Step 3: Install Build Tools (One-Time Setup)
🔹 Install Visual C++ Build Tools:
- Go to:
```
 https://visualstudio.microsoft.com/visual-cpp-build-tools/
```
During installation, select:
- ✅ C++ build tools
- ✅ Windows 10 SDK / Windows 11 SDK
- ✅ CMake tools for Windows

[Example image](assets/Install_Build_Tools.jpg)

These are required to build dlib, a dependency of face_recognition.
### NOTE
- you will have to do step 4 even though you have already tick that(✅ CMake tools for Windows) option during Instalation Visual C++ Build Tools
- (✅ Windows 10 SDK / Windows 11 SDK) depends on your operating system

## ✅ Step 4: Install CMake (if not installed)
🔹 Download from:
- Go to:
```
https://cmake.org/download/
```
[Example image](assets/cmake_download.jpg)
- Install and make sure CMake is added to PATH during installation.[Example image](assets/instalation_cmake.jpg)
- Confirm CMake installation:
```
cmake --version
```
You should see something like:
```
cmake version 3.29.2
```


## ✅ Step 5: Install dlib (core dependency)
Option 1: Install via pip (works with Python 3.6–3.10)
```
pip install dlib==19.24.2
```
Option 2: (If pip install fails) Install precompiled dlib from github
1. Visit github page to download dlib (for python 3.10)
```
https://github.com/z-mahmud22/Dlib_Windows_Python3.x/blob/main/dlib-19.22.99-cp310-cp310-win_amd64.whl
```
- keep downloaded dlib file in same directory with project

Example install:
[Example image](assets/dlib_instalation.png)

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











