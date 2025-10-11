# Optimization Windows OS

### <a name="Goals"></a> Goals


> * optimization windows os.

> [!IMPORTANT]
> use `command prompt` to write this commands ( Run it as Administrator ).

</p>
<h3 align="center">Auto-Updates: Drivers, Programs & Apps</h3>
<p align="center">
</p>

> These three commands are used to keep your system and Python environment up to date. The first command, `winget upgrade --all`, uses the Windows Package Manager to automatically upgrade all applications installed via winget, such as browsers, code editors, or productivity tools. The second command, `pip install --upgrade pip`, updates Python’s package installer itself (pip) to the latest version, which is important for compatibility with newer packages and features. Finally, `pip install pip-review` installs a tool called pip-review, which helps you identify and manage outdated Python packages. Once installed, you can run `pip-review --auto` to automatically upgrade all outdated Python libraries in your environment, streamlining the update process for your development tools.

```shell
winget upgrade --all
pip install --upgrade pip
pip install pip-review
```

</p>
<h3 align="center">Diagnose: repair the system image</h3>
<p align="center">
</p>

> The DISM commands are used to diagnose and repair issues with the Windows system image, which is essential when the operating system behaves abnormally or system files become corrupted. The command `DISM /Online /Cleanup-Image /CheckHealth` performs a quick scan to determine if the system image is flagged as corrupt and whether it can be repaired. It's fast and useful for an initial check. If you want a more thorough inspection, `DISM /Online /Cleanup-Image /ScanHealth` conducts a deeper analysis to detect any corruption within the system image, although it does not attempt any repairs. Finally, `DISM /Online /Cleanup-Image /RestoreHealth` is the command that actively attempts to repair any detected issues by downloading clean system files from Windows Update and replacing the corrupted ones. Running these commands in sequence ensures that your Windows installation remains stable, healthy, and functional.

```shell
DISM /Online /Cleanup-Image /ScanHealth
DISM /Online /Cleanup-Image /CheckHealth
DISM /Online /Cleanup-Image /RestoreHealth
```

> [!NOTE]
> These commands take a few minutes to finish.
> 

</p>
<h3 align="center">SFC: System File Checker</h3>
<p align="center">
</p>

> The `sfc` (System File Checker) commands are used to scan the integrity of system files in Windows and ensure they haven't been corrupted or tampered with. The command `sfc /scannow` performs a full scan of all protected system files and automatically attempts to repair any corrupted or missing files using a cached copy stored by Windows. It's the go-to command when you're experiencing system instability or suspect file corruption. On the other hand, `sfc /verifyonly` checks for file integrity issues **without making any changes or repairs**. It’s a safe, read-only diagnostic option to verify if there's a problem before deciding to fix it. Both commands help maintain system reliability and are often used alongside DISM for deeper system repair.

```shell
sfc /scannow
sfc /verifyonly
```

</p>
<h3 align="center">Clean up unnecessary files: free up space on your Windows system</h3>
<p align="center">
</p>

> These two commands are used to clean up unnecessary files and free up space on your Windows system.
The first command, `del /s /q %temp%\*`, deletes all files and folders inside the user's temporary files directory. The `/s` switch tells it to delete files in all subdirectories, and `/q` enables quiet mode so it doesn’t prompt for confirmation. This is a quick and effective way to clear out clutter that builds up from software installations, browser caches, and background processes.
The second command, `cleanmgr`, launches the built-in Windows Disk Cleanup utility. It provides a graphical interface where you can choose which types of files to remove (e.g., recycle bin, system temp files, Windows update leftovers). Used together, these commands help speed up the system and reclaim storage space by removing digital junk.

```shell
del /s /q %temp%\*
del /q /f /s %temp%\*
del /q /f /s C:\Windows\Temp\*
for /d %x in (%temp%\*) do @rd /s /q "%x"
for /d %x in (C:\Windows\Temp\*) do @rd /s /q "%x"
cleanmgr
```

> [!WARNING]
> Do not close the `cmd` until all processes have finished.


</p>
<h3 align="center">Copyright © 2025</h3>
<p align="center">
</p>

> Thank you for reaching out to us here. If you have any feedback, feel free to contact us at:
tknohamzacontact@gmail.com
Don't forget to follow us on:
<a href="https://facebook.com/tknohamza">Facebook</a>, <a href="https://instagram.com/r/tknohamza">Instagram</a>, <a href="https://twitter.com/tknohamza">Twitter</a>, <a href="https://t.me/tknohamzachannel">Telegram</a>
