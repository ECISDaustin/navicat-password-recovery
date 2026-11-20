# Navicat Password Recovery

Small Python utilities for recovering passwords saved in Navicat connection
profiles.

## Requirements

- Python 3
- The dependency listed in `requirements.txt` (`pycryptodome`)

Install the dependency from PowerShell:

```powershell
py -m pip install -r requirements.txt
```

## Scripts

- `NavicatCipher.py` encrypts or decrypts a ciphertext value. Add `-ncx` when
  handling values prepared for or exported from an NCX file.
- `NcxReader.py` reads a Navicat NCX export and displays its connection details.
- `ShowNavicat.py` reads saved Navicat server profiles from the current Windows
  user's registry. This script is Windows-only.

Run a script with Python, for example:

```powershell
py .\NavicatCipher.py dec <ciphertext>
py .\NavicatCipher.py dec -ncx <ciphertext>
py .\NcxReader.py <path-to-ncx-file>
py .\ShowNavicat.py
```

Use these tools only with connection profiles you own or are authorized to
access. Their output can include database and SSH passwords; treat it as
sensitive and do not share or commit it.
