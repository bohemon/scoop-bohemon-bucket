# scoop-bohemon-bucket

[![CI](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/ci.yml)
[![Excavator](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/excavator.yml)

A personal bucket for [Scoop](https://scoop.sh/), the Windows command-line installer.

## Available manifests

| Manifest | Description | How to launch |
| --- | --- | --- |
| `effetune` | Real-time audio effect processor for enhancing music listening | Open **EffeTune** from the Start menu |
| `elecom-mouse-assistant-np` | Button, gesture, and profile settings for supported ELECOM mice (non-portable) | Open **ELECOM Mouse Assistant 6** from the Start menu |
| `mozkey-ibg-np` | Mozkey/Mozc-based Japanese input method with Grimodex integration (non-portable) | Select **Mozkey IbG** from the Windows input method selector |
| `rom-converto` | CLI for converting, compressing, verifying, encrypting, and decrypting ROMs and disc images | Run `rom-converto` |
| `rom-converto-gui` | Desktop GUI for rom-converto | Open **rom-converto** from the Start menu |

All manifests target Windows x64. The rom-converto CLI and GUI versions can be installed side by side.

## Usage

Add this bucket from PowerShell after installing Scoop:

```powershell
scoop bucket add bohemon https://github.com/bohemon/scoop-bohemon-bucket
```

Install EffeTune:

```powershell
scoop install bohemon/effetune
```

Install ELECOM Mouse Assistant 6:

```powershell
scoop install bohemon/elecom-mouse-assistant-np
```

The `-np` suffix denotes a non-portable package. Administrator approval is required to extract the official installer and install its MSI. The application is installed under Program Files with system-wide drivers, Start menu and desktop shortcuts, and a startup shortcut. Restart Windows after uninstalling to finish removing driver registrations. Use Scoop for application updates, and uninstall Mouse Assistant 5 or older InstallShield-based versions before installing this package.

Install Mozkey IbG for Windows x64:

```powershell
scoop install bohemon/mozkey-ibg-np
```

This non-portable package requires Windows 10 1809 or later and administrator approval. It runs the official MSI to install the IME, its service, and firewall rules system-wide. Upstream distributes unsigned experimental prereleases intended for Grimodex integration; review the [project's warnings](https://github.com/kazormia296/mozkey-ibg#readme) before use. A sign-out or restart may be needed before selecting the IME. Use Scoop for updates and removal, and restart Windows after uninstalling; the manifest does not restart Windows automatically. Settings and learned data remain in the application's own user profile rather than Scoop's persist directory.

Install the rom-converto CLI:

```powershell
scoop install bohemon/rom-converto
rom-converto --help
```

Install the rom-converto GUI:

```powershell
scoop install bohemon/rom-converto-gui
```

## Updating

Update Scoop and its buckets, then update the installed applications:

```powershell
scoop update
scoop update effetune elecom-mouse-assistant-np mozkey-ibg-np rom-converto rom-converto-gui
```

GitHub Actions periodically runs Excavator to check the manifests for new releases.

## Contributing

Bug reports and manifest improvements are welcome through [issues](https://github.com/bohemon/scoop-bohemon-bucket/issues) and pull requests.
When modifying a manifest, please also refer to Scoop's [App Manifests documentation](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests).

## License

This bucket is available under the [MIT License](LICENSE). Each application remains subject to the license specified by its publisher.
