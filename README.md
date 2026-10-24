# Extenject (Larje UPM package)

Extenject 9.2.0 (https://github.com/Mathijs-Bakker/Extenject), the maintained fork of Zenject by Modest Tree Media, repackaged as a Unity Package Manager git package.

## Install

Add to `Packages/manifest.json`:

```json
"com.larje.extenject": "https://github.com/danil777lar/com.larje.extenject.git#9.2.0"
```

Remove `Assets/Plugins/Zenject` first if Extenject was imported from the Asset Store, otherwise the assemblies conflict.

## Contents

| Folder | Assembly | Notes |
|---|---|---|
| `Runtime` | `Zenject` | Core container, installers, contexts, factories, pools, Signals |
| `Editor/Core` | `Zenject-Editor` | Inspectors and menu items |
| `Editor/MemoryPoolMonitor` | `Zenject-PoolMonitor-Editor` | Window > Zenject Pool Monitor |
| `Editor/ReflectionBaking` | `Zenject-ReflectionBaking-Editor` | Optional IL weaving for faster injection |
| `TestFramework` | `Zenject-TestFramework` | `ZenjectUnitTestFixture`, `ZenjectIntegrationTestFixture` |

Sample games, internal unit/integration tests and AutoMocking archives from the Asset Store package are not included.

Larje packages detect this package through `versionDefines` and enable their `Larje.*.Zenject` installer assemblies automatically.

## Local changes

- `Runtime/Source/Util/UnityUtil.cs`, `Runtime/Source/Install/Contexts/ProjectContext.cs`: deprecated `FindObjectsOfType` replaced with `FindObjectsByType` (sort-mode overload before Unity 6000.4).

## License

MIT, see `LICENSE.md`. Copyright (c) 2010-2015 Modest Tree Media, Extenject contributors.
