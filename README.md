# coxfordmc/modpacks

Every Coxford modpack lives here, one directory per pack under `packs/`, in
[packwiz](https://packwiz.infra.link/) format. Pushing to `main` builds each pack
into a `.mrpack` and attaches it to a GitHub release, so the download links below
never change.

```
packs/
  example/           <- template pack, MC 26.2 / Fabric
    pack.toml
    index.toml
    mods/
      fabric-api.pw.toml
      lithium.pw.toml
      sodium.pw.toml
```

## Install links

One paste-able link per pack. Both launchers take a URL directly — no file to
download by hand.

| Pack | Direct link |
| --- | --- |
| example | `https://github.com/coxfordmc/modpacks/releases/latest/download/example.mrpack` |

**Prism Launcher** — Add Instance → Import → paste the link → OK.
**Modrinth App** — it accepts the same `.mrpack` URL, or download it and open it.

## Starting a new pack

```bash
cp -r packs/example packs/newpack
cd packs/newpack
$EDITOR pack.toml          # name, version, description; bump minecraft/fabric if needed
packwiz refresh
```

Then commit. The workflow picks up any directory under `packs/`, so the new pack's
link is `.../releases/latest/download/newpack.mrpack` from the first build.

## Adding and updating mods

Always use packwiz rather than editing the `.pw.toml` files by hand — it writes the
pinned version and hash and keeps `index.toml` consistent.

```bash
cd packs/example
packwiz modrinth add sodium      # or: packwiz mr add <url or slug>
packwiz curseforge add <slug>    # CurseForge-only mods
packwiz update --all             # pull newer versions of everything
packwiz refresh                  # rebuild index.toml after any manual change
```

`side` in each `.pw.toml` controls where the mod is installed: `both`, `client`, or
`server`. Client-only performance and visual mods should be `client` so the server
side stays clean.

Config files, resource packs and so on go in the pack directory the same way they
sit in a `.minecraft` folder (`config/`, `resourcepacks/`, `shaderpacks/`) and get
tracked with `packwiz refresh`.

## Installing packwiz locally

```bash
go install github.com/packwiz/packwiz@latest
```

## What's in the example pack

Minecraft 26.2, Fabric Loader 0.19.5, three mods that most packs want anyway:

- **Fabric API** (`both`) — required by nearly every Fabric mod
- **Lithium** (`both`) — general tick/server performance
- **Sodium** (`client`) — rendering performance

Swap them out; the point of the directory is the structure, not the mod list.
