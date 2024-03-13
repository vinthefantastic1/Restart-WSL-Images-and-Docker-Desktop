# Restart WSL Images and Docker Desktop

This guide provides instructions on how to restart WSL (Windows Subsystem for Linux) images and Docker Desktop. 

Run these commands from an administrator command prompt.

1. `taskkill /f /im wslservice.exe`: This command forcefully terminates the WSL service.
2. `taskkill /f /im wslhost.exe`: This command forcefully terminates the WSL host process.
3. `taskkill /f /im wsl.exe`: This command forcefully terminates the WSL process.
4. `sc.exe queryex LxssManager`: This command queries the status of the LxssManager service.
5. `sc.exe stop LxssManager`: This command stops the LxssManager service.
6. `sc.exe start LxssManager`: This command starts the LxssManager service.
7. `sc.exe queryex LxssManager`: This command queries the status of the LxssManager service again.
8. `wsl --shutdown`: This command shuts down all running WSL instances.
9. `wsl ~`: This command starts a new WSL instance. (If this doesn't work you may need to reboot and try again)

After the previous steps complete:
- Run Docker Desktop as an administrator.
