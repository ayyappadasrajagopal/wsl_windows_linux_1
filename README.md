# wsl_windows_linux_1

## Install WSL on windows
https://learn.microsoft.com/en-us/windows/wsl/install

## WSL extension for visual studio code on windows
https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl

## Visual studio code with WSL
https://code.visualstudio.com/docs/remote/wsl


## Setting up multiple WSL distribution instances

# Setting Up Multiple WSL Distributions on Windows

This guide explains how to install and manage multiple **WSL (Windows Subsystem for Linux)** distributions on your Windows machine.

---

## 1. Install WSL

Open **PowerShell as Administrator** and run:

```powershell
wsl --install
```

Check version:

```powershell
wsl --version
```

---

## 2. List Available Distributions

```powershell
wsl --list --online
```

Example output:

```
NAME            FRIENDLY NAME
Ubuntu          Ubuntu
Debian          Debian GNU/Linux
kali-linux      Kali Linux Rolling
openSUSE-42     openSUSE Leap 42
Alpine          Alpine Linux
```

---

## 3. Install Additional Distributions

```powershell
wsl --install -d <DistributionName>
```

Examples:

```powershell
wsl --install -d Debian
wsl --install -d kali-linux
```

---

## 4. View Installed Distributions

```powershell
wsl --list --verbose
```

Example:

```
  NAME            STATE           VERSION
* Ubuntu          Running         2
  Debian          Stopped         2
  kali-linux      Stopped         2
```

---

## 5. Launch Specific Distribution

```powershell
wsl -d <DistroName>
```

Examples:

```powershell
wsl -d Ubuntu
wsl -d Debian
```

---

## 6. Set Default Distribution

```powershell
wsl --set-default <DistroName>
```

Example:

```powershell
wsl --set-default Debian
```

---

## 7. Export / Import Distributions (Optional)

Export a distribution:

```powershell
wsl --export <DistroName> <FilePath>
```

Import a distribution:

```powershell
wsl --import <NewDistroName> <InstallLocation> <FilePath>
```

---

### Set WSL Version

Ensure distros use WSL 2 (recommended):

```powershell
wsl --set-version <DistroName> 2
```

Example:

```powershell
wsl --set-version Ubuntu 2
```

---

✅ Now you can have multiple isolated Linux environments running side by side in WSL!


## CUDA on WSL User Guide
https://docs.nvidia.com/cuda/wsl-user-guide/index.html


## Enable NVIDIA CUDA on WSL
https://learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl
