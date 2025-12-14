# render-demo

Minimal Flask app for deployment demos.

Quick start (local):

1. Create and activate a virtual environment (PowerShell may require adjusting execution policy).

```powershell
python -m venv myenv
Set-Location 'C:\Users\Laptop Walah\Desktop\render-demo'
. .\myenv\Scripts\Activate.ps1   # dot-source to run in current session
pip install -r requirements.txt
python app.py
```

Or for local dev without venv:

```powershell
pip install -r requirements.txt
python app.py
```

Deploy: the included `Procfile` uses `gunicorn app:app` (Render/Heroku). On Linux-based hosts use that as the start command.

If PowerShell blocks `Activate.ps1`, either run `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` for the session, or run the batch script `myenv\Scripts\activate.bat` from `cmd`.
