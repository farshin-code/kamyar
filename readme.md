Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Restart-Computer
Set-ExecutionPolicy RemoteSigned
Add-AppxPackage .\Ubuntu.appx
wsl --list --verbose

https://learn.microsoft.com/windows/wsl/install-manual


$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")

