
HIT137 — Group Assignment 3
Tkinter AI GUI (Hugging Face models)

Short description:
This project is a Tkinter desktop GUI that integrates three Hugging Face models (text, image, audio) and demonstrates OOP concepts required by the assignment (multiple inheritance, multiple decorators, encapsulation, polymorphism, method overriding). The GUI allows the user to choose input type (Text / Image / Audio), load or type input, run one or both models, view structured + raw outputs, read OOP explanations, and see model info. The app includes a circular loading overlay (blue message inside) and a red-styled error popup for exceptions.

----------------------------------------------------------------
Table of contents
----------------------------------------------------------------
1. What this repository contains
2. How the project meets the assignment requirements
3. System requirements
4. Quick install & run (Windows, CMD)
5. Detailed install steps (commands to copy/paste)
6. How to run the GUI
7. Files & project structure explained
8. How to test models (small test scripts)
9. Screenshots — where to put images & how to add them to README
10. GitHub & submission instructions (what graders want)
11. Troubleshooting (common errors and fixes)
12. Notes and extension ideas
13. License & credits

----------------------------------------------------------------
1. What this repository contains
----------------------------------------------------------------
A multi-file Python Tkinter app designed to live in a folder such as:
project/
├─ main.py
├─ models.py
├─ gui_components.py
├─ utils.py
├─ explanations.py
├─ README.md
├─ github_link.txt
├─ README.txt
└─ assets/
   └─ screenshots/

----------------------------------------------------------------
2. How the project meets the assignment requirements
----------------------------------------------------------------
- Three Hugging Face models integrated (text, image, audio).
- Dropdown & file selectors for text, image, audio input.
- Outputs shown in structured + raw formats.
- OOP concepts applied (multiple inheritance, multiple decorators, encapsulation, polymorphism, method overriding).
- Explanations included in code + separate section.
- GUI supports model info, error popups, and loader overlay.

----------------------------------------------------------------
3. System requirements
----------------------------------------------------------------
- OS: Windows (works also on Linux/Mac with minor changes)
- Python 3.10+
- Disk space for model downloads (50–300 MB per model)
- Internet required first time
- Optional: ffmpeg for MP3

----------------------------------------------------------------
4. Quick install & run (Windows CMD)
----------------------------------------------------------------
cd C:\Users\ADMIN\Desktop
mkdir project
cd project
python -m venv venv
venv\Scripts\activate
pip install --upgrade pip setuptools wheel
pip install transformers pillow requests tqdm numpy SoundFile librosa
pip install --index-url https://download.pytorch.org/whl/cpu/ torch torchaudio --extra-index-url https://pypi.org/simple
python main.py

----------------------------------------------------------------
5. Detailed install steps (commands to copy/paste)
----------------------------------------------------------------
1. Clone/download repo to C:\Users\ADMIN\Desktop\project
2. Create venv: python -m venv venv
3. Activate: venv\Scripts\activate
4. Upgrade pip & install deps (see above)
5. Run: python main.py

----------------------------------------------------------------
6. How to run the GUI
----------------------------------------------------------------
- Activate venv: venv\Scripts\activate
- Run: python main.py
- Choose input type (text/image/audio)
- Load file or type text
- Run models
- Save outputs or view explanations

----------------------------------------------------------------
7. Files & project structure explained
----------------------------------------------------------------
main.py — entry point
models.py — AI models with OOP concepts
gui_components.py — Tkinter GUI, loader, error popup
utils.py — helpers + decorators
explanations.py — OOP explanations + model info
github_link.txt — contains your repo URL
assets/screenshots/ — place screenshots here

----------------------------------------------------------------
8. How to test models (small test scripts)
----------------------------------------------------------------
Example (text):
from transformers import pipeline
pipe = pipeline("sentiment-analysis", model="distilbert-base-uncased-finetuned-sst-2-english")
print(pipe("I love this project"))

----------------------------------------------------------------
9. Screenshots — where to put images
----------------------------------------------------------------
Put in: project/assets/screenshots/
Add them in README.md with:
![Main window](assets/screenshots/1-main.png)

----------------------------------------------------------------
10. GitHub & submission instructions
----------------------------------------------------------------
- Public repo required
- Add groupmates as collaborators
- Commit all files
- Add repo link to github_link.txt
- Zip project folder and upload to Learnline

----------------------------------------------------------------
11. Troubleshooting (common errors and fixes)
----------------------------------------------------------------
1. UnidentifiedImageError: Wrong file type, use correct input.
2. ffmpeg not found: install ffmpeg or use WAV audio.
3. Torch device mismatch: reinstall CPU-only torch wheel.
4. Slow downloads: wait for Hugging Face cache.
5. Missing soundfile: pip install SoundFile librosa numpy

----------------------------------------------------------------
12. Notes and extension ideas
----------------------------------------------------------------
- Progress bars for downloads
- Cancel button for tasks
- More models (text-to-image, etc)
- Add CI tests on GitHub Actions

----------------------------------------------------------------
13. License & credits
----------------------------------------------------------------
- Educational code for HIT137 course
- Models from Hugging Face (see explanations.py)
