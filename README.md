![Platform](https://img.shields.io/badge/platform-Windows-blue)
![License](https://img.shields.io/github/license/sucktravian/ControlUpgrade)
![Built with](https://img.shields.io/badge/built%20with-WPF%20%7C%20.NET%209-blueviolet)

# Windows Upgrade Control


[⬇️ Download Latest Release](https://github.com/sucktravian/ControlUpgrade/releases/latest)

A simple WPF app I built to make it easier to block or unblock Windows upgrades using registry keys. It comes with a clean interface, dark mode toggle, and some basic localization (English and Japanese).

I mainly made this to avoid digging through the registry manually every time. Sharing it in case it's useful to others too.

## Features

- 🔒 Lock/unlock Windows upgrade behavior  
- 🌗 Toggle between light and dark mode  
- 🧾 View and open relevant registry keys  
- 🌐 Localized (English 🇺🇸 / Japanese 🇯🇵)  
- 🎞 Animated status bar just for fun

## Requirements

- Windows 10 or 11  
- No .NET install required when using the portable release

## Portable build

Publish the portable Windows x64 package with:

```powershell
dotnet publish .\ControlUpgrade\ControlUpgrade.csproj /p:PublishProfile=Portable-win-x64
```

Pack the files from:

```text
ControlUpgrade\bin\Release\net9.0-windows\win-x64\publish\portable\
```

This output is self-contained, so Windows should not ask users to download the .NET Desktop Runtime.

## Release publishing

To publish a new GitHub release, update the `<Version>` value in `ControlUpgrade/ControlUpgrade.csproj`, then commit and push to `main` or `master`.

GitHub Actions will build the portable package and create a release named after that version, such as `v1.0.0`. If that release already exists, the workflow skips publishing.

## License

Released under the [GPL v3](LICENSE).  
You’re free to use, share, and modify it — just don’t resell it or remove my name from the code.

---

This is something I use personally, so it’s not enterprise-grade — but it works well and is open to feedback or improvement!

## Screenshots

### Light Mode
![Light Theme](screenshots/MainMenu_Light.png)

### Dark Mode
![Dark Theme](screenshots/MainMenu_Dark.png)

### Upgrade Tab
![Upgrade Tab](screenshots/UpgradeBlock.png)

### Registry Tab
![Registry Tab](screenshots/RegistryOpen.png)

