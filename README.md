# scoop-bohemon-bucket

[![CI](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/ci.yml)
[![Excavator](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/excavator.yml)

A personal bucket for [Scoop](https://scoop.sh/), the Windows command-line installer.

## Available manifests

| Manifest | Description | How to launch |
| --- | --- | --- |
| `effetune` | Real-time audio effect processor for enhancing music listening | Open **EffeTune** from the Start menu |
| `ps3-disc-dumper` | Utility for creating decrypted PS3 disc dumps | Open **PS3 Disc Dumper** from the Start menu |
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

Install PS3 Disc Dumper:

```powershell
scoop install bohemon/ps3-disc-dumper
```

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
scoop update effetune ps3-disc-dumper rom-converto rom-converto-gui
```

GitHub Actions periodically runs Excavator to check the manifests for new releases.

## Contributing

Bug reports and manifest improvements are welcome through [issues](https://github.com/bohemon/scoop-bohemon-bucket/issues) and pull requests.
When modifying a manifest, please also refer to Scoop's [App Manifests documentation](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests).

## License

This bucket is available under the [MIT License](LICENSE). Each application remains subject to the license specified by its publisher.
