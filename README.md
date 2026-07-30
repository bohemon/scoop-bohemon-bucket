# scoop-bohemon-bucket

[![CI](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/ci.yml)
[![Excavator](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/bohemon/scoop-bohemon-bucket/actions/workflows/excavator.yml)

A personal bucket for [Scoop](https://scoop.sh/), the Windows command-line installer.
It currently provides both the CLI and GUI versions of [rom-converto](https://github.com/DevYukine/rom-converto).

## Available manifests

| Manifest | Description | How to launch |
| --- | --- | --- |
| `rom-converto` | CLI for converting, compressing, verifying, encrypting, and decrypting ROMs and disc images | Run `rom-converto` |
| `rom-converto-gui` | Desktop GUI for rom-converto | Open **rom-converto** from the Start menu |

Both manifests target Windows x64. The CLI and GUI versions can be installed side by side.

## Usage

Add this bucket from PowerShell after installing Scoop:

```powershell
scoop bucket add bohemon https://github.com/bohemon/scoop-bohemon-bucket
```

Install the CLI:

```powershell
scoop install bohemon/rom-converto
rom-converto --help
```

Install the GUI:

```powershell
scoop install bohemon/rom-converto-gui
```

## Updating

Update Scoop and its buckets, then update the installed applications:

```powershell
scoop update
scoop update rom-converto rom-converto-gui
```

GitHub Actions periodically runs Excavator to check the manifests for new releases.

## Contributing

Bug reports and manifest improvements are welcome through [issues](https://github.com/bohemon/scoop-bohemon-bucket/issues) and pull requests.
When modifying a manifest, please also refer to Scoop's [App Manifests documentation](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests).

## License

This bucket is available under the [MIT License](LICENSE). Each application remains subject to the license specified by its publisher.
