<h1>ಪ್ರಾರಂಭಿಸಲಾಗುತ್ತಿದೆ</h1>

<h4> ಈ ಡಾಕ್ಯುಮೆಂಟ್ ಸಿಂಹನಾರಿಯೊಂದಿಗೆ ಕೆಲಸ ಮಾಡಲು ಸ್ಟೇಜಿಂಗ್ ಪರಿಸರವನ್ನು ಹೇಗೆ ರಚಿಸುವುದು ಮತ್ತು ಡಾಕ್ಸ್ ಅನ್ನು ಓದುವುದು ಹೇಗೆ ಎಂದು ತೋರಿಸುತ್ತದೆ </h4>

1. ನೀವು ಈಗಾಗಲೇ ಪೈಥಾನ್ ಹೊಂದಿದ್ದೀರಿ ಎಂದು ಊಹಿಸಿ, ಸಿಂಹನಾರಿ ಅನ್ನು ಸ್ಥಾಪಿಸಿ. ಇಲ್ಲದಿದ್ದರೆ, ದಯವಿಟ್ಟು [ಸ್ಟೆಪ್ಸ್](https://realpython.com/installing-python/) ಅನುಸರಿಸಿ tp ಪೈಥಾನ್ ಅನ್ನು ಸ್ಥಾಪಿಸಿ. ನಂತರ ಮಾಡಿ:

```bash
pip3 install sphinx sphinx-autobuild
```

2. ನಿಮ್ಮ ಡಾಕ್ಸ್ ಅನ್ನು ಹಿಡಿದಿಡಲು ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್‌ನಲ್ಲಿ ಡೈರೆಕ್ಟರಿಯನ್ನು ರಚಿಸಿ:

```bash
cd /path/to/project
mkdir docs
```

3. ಅಲ್ಲಿ ಸಿಂಹನಾರಿ-ಕ್ವಿಕ್‌ಸ್ಟಾರ್ಟ್ ಅನ್ನು ರನ್ ಮಾಡಿ:

```bash
cd docs
sphinx-quickstart
```

4. ಇದು ಮೂಲಭೂತ ಸಂರಚನೆಯನ್ನು ರಚಿಸುವ ಮೂಲಕ ನಿಮ್ಮನ್ನು ಕರೆದೊಯ್ಯುತ್ತದೆ; ಹೆಚ್ಚಿನ ಸಂದರ್ಭಗಳಲ್ಲಿ, ನೀವು ಡೀಫಾಲ್ಟ್‌ಗಳನ್ನು ಸ್ವೀಕರಿಸಬಹುದು. ಇದು ಪೂರ್ಣಗೊಂಡಾಗ, ನೀವು *index.rst*, *conf.py* ಮತ್ತು ಕೆಲವು ಇತರ ಫೈಲ್‌ಗಳನ್ನು ಹೊಂದಿರುತ್ತೀರಿ. ಪರಿಷ್ಕರಣೆ ನಿಯಂತ್ರಣಕ್ಕೆ ಇವುಗಳನ್ನು ಸೇರಿಸಿ. ಈಗ, ನಿಮ್ಮ *index.rst* ಅನ್ನು ಸಂಪಾದಿಸಿ ಮತ್ತು ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್ ಕುರಿತು ಕೆಲವು ಮಾಹಿತಿಯನ್ನು ಸೇರಿಸಿ. ನೀವು ಇಷ್ಟಪಡುವಷ್ಟು ವಿವರಗಳನ್ನು ಸೇರಿಸಿ. ಅವರು ಹೇಗೆ ಕಾಣುತ್ತಾರೆ ಎಂಬುದನ್ನು ನೋಡಲು ಅವುಗಳನ್ನು ನಿರ್ಮಿಸಿ:

```
make html
```

**ಗಮನಿಸಿ:** *ನಿಮ್ಮ ಡಾಕ್ಸ್ ಅನ್ನು ಸ್ವಯಂ-ರೀಲೋಡ್ ಮಾಡಲು ನೀವು ಸಿಂಹನಾರಿ-ಆಟೋಬಿಲ್ಡ್ ಅನ್ನು ಬಳಸಬಹುದು. ಸಿಂಹನಾರಿ-ಆಟೋಬಿಲ್ಡ್ ಅನ್ನು ರನ್ ಮಾಡಿ. ಬದಲಿಗೆ _build/html.*

5. ಸಂಬಂಧಿತ ಕೋಡ್ ಫೈಲ್‌ಗಳನ್ನು ಮಾತ್ರ ಪ್ರಕಟಿಸಲು ಆದರೆ ಬಿಲ್ಡ್, _static & _templates ಡೈರೆಕ್ಟರಿಗಳನ್ನು ಪ್ರಕಟಿಸಲು - ದಯವಿಟ್ಟು ರೂಟ್ ಡೈರೆಕ್ಟರಿಯಲ್ಲಿ .gitignore ಅನ್ನು ಸೇರಿಸಿ. ಒಂದು ಮಾದರಿ ಕೆಳಗೆ ಇದೆ

```python
#Folders to ignore
build
_templates
_static

#Extensions to ignore
*.pyc
*.diff
*.err
*.orig
*.rej
*.swo
*.swp
*.vi
*.cache
*.egg-info
*~
*#

#Logs and database files to be ignored
*.log
*.sql
*.sqlite

#OS or Editor folders
.DS_Store
Thumbs.db
.cache
.project
.settings
.tmproj
*.esproj
nbproject
*.sublime-project
```

6. ನೀವು ನೋಡುವುದನ್ನು ನೀವು ಇಷ್ಟಪಡುವವರೆಗೆ ಮರುನಿರ್ಮಾಣ ಮಾಡಲು ನಿಮ್ಮ ಫೈಲ್‌ಗಳನ್ನು ಸಂಪಾದಿಸಿ, ನಂತರ ನಿಮ್ಮ ಬದಲಾವಣೆಗಳನ್ನು ಮಾಡಿ ಮತ್ತು ನಿಮ್ಮ ಸಾರ್ವಜನಿಕ ರೆಪೊಸಿಟರಿಗೆ ತಳ್ಳಿರಿ. ಒಮ್ಮೆ ನೀವು ಸಾರ್ವಜನಿಕ ರೆಪೊಸಿಟರಿಯಲ್ಲಿ **Sphinx** ದಸ್ತಾವೇಜನ್ನು ಹೊಂದಿದ್ದರೆ, ನೀವು **ಡಾಕ್ಸ್ ಓದಿ** ಅನ್ನು ಬಳಸಲು ಪ್ರಾರಂಭಿಸಬಹುದು.