# 🌦️ WTTRTerminal
Get Weather in Your Terminal by using wttr.in

## 🪟 Windows Setup
To edit the PowerShell profile, follow these steps:

1.  **Open Notepad** or your preferred text editor.
2.  Navigate to: `C:\Users\Username\Documents\PowerShell\`
3.  Open: `Microsoft.PowerShell_profile.ps1`
4.  Add this function:

```powershell
function weather {
    Invoke-RestMethod https://wttr.in
}
```

5. 💾 **Save** the file.
6. 🔄 **Reload** the profile by running:

```powershell
. $PROFILE
```

✅ Now, check the weather with:
```powershell
weather
```

---
## 🐧 Linux Setup
For Bash users, add the following to your bash profile (e.g., `~/.bashrc` or `~/.bash_profile`):

```bash
# Weather Function
_weather(){
   curl -s -L wttr.in/$@ | less -R
}
alias weather='_weather'
```

💾 Reload the profile with:
```bash
source ~/.bashrc
```

✅ Now, you can view the weather by typing:
```bash
weather , or weather [location]
```



