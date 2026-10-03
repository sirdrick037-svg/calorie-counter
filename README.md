# Calorie Counter

A small Django app for recording food and tracking today's calorie total.

## Run locally on Windows

From this directory in PowerShell:

```powershell
py -m venv myenv
.\myenv\Scripts\python.exe -m pip install -r requirements.txt
if (-not (Test-Path .\calorie_tracker\.env)) {
    Copy-Item .\calorie_tracker\.env.example .\calorie_tracker\.env
}
```

Before running the app for the first time, replace the example `SECRET_KEY` in
`calorie_tracker\.env` with a unique value. If `calorie_tracker\.env` already
exists, keep its existing key.

```powershell
.\myenv\Scripts\python.exe .\manage.py migrate
.\myenv\Scripts\python.exe .\manage.py runserver
```

Open <http://127.0.0.1:8000/>. The project is configured for local development;
set `DEBUG` to `False` and configure production settings before deployment.
