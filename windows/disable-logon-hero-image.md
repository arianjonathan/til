#Use a Single Color Instead of an Image

Rather than seeing a background image whenever you type your password, you can choose to disable the login screen background and see a single, flat-color background — just as Windows 8 and 8.1 used. This requires a quick registry tweak.

Open the Registry Editor and create a `DWORD` value named “DisableLogonBackgroundImage” under “HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\System” with the value “00000001”. Delete the value or set it to “00000000” to go back to the default Windows 10 “hero image.”

After you perform the registry hack, the Windows login screen will disiplay a flat-color background behind the login prompt. Just press `Windows Key + L` to lock your PC and check. You don’t have to reboot.