Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Restart-Computer
Set-ExecutionPolicy RemoteSigned
Add-AppxPackage .\Ubuntu.appx
wsl --list --verbose

