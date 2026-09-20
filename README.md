# coxfordmc/modpacks

Every Coxford modpack lives here, one directory per pack under `packs/`, in
[packwiz](https://packwiz.infra.link/) format. Pushing to `main` builds each pack
into a `.mrpack` and attaches it to a GitHub release, so the download links below
never change.

```
packs/
  example/           template — copy this to start a new pack
  creative-preset/   client-side preset for Not-Boring Creative (shaders)
  survival/          both-sides performance pack
```

## Install links

One paste-able link per pack. Both launchers take a URL directly — no file to
download by hand.

| Pack | Direct link |
| --- | --- |
| example | `https://github.com/coxfordmc/modpacks/releases/latest/download/example.mrpack` |
| creative-preset | `https://github.com/coxfordmc/modpacks/releases/latest/download/creative-preset.mrpack` |
| survival | `https://github.com/coxfordmc/modpacks/releases/latest/download/survival.mrpack` |

**Prism Launcher** — Add Instance → Import → paste the link → OK.
**Modrinth App** — it accepts the same `.mrpack` URL, or download it and open it.

## The packs

**example** — MC 26.2 / Fabric 0.19.5, three deliberately boring mods (Fabric API,
Lithium, Sodium). The point of the directory is the structure, not the mod list.

**creative-preset** — everything is `side = "client"`. Not-Boring Creative is vanilla
Paper, so none of this is required to join; it's a prepackaged instance for people
who want shaders without assembling one. Ships Iris + Sodium, Complementary Unbound
as a shaderpack, Better Leaves as a resource pack, and config that turns both on out
of the box.

**survival** — same mod list on both sides (Fabric API, Lithium, FerriteCore,
Krypton). The server's own mods come from this same directory, so the two can't
drift apart.

## Adding mods, shaders, and resource packs

All three are the same operation. packwiz reads the project type from Modrinth and
files it in the right folder — `mods/`, `shaderpacks/`, `resourcepacks/`, `datapacks/`:

```bash
cd packs/creative-preset
packwiz modrinth add sodium                    # -> mods/sodium.pw.toml
packwiz modrinth add complementary-unbound     # -> shaderpacks/complementary-unbound.pw.toml
packwiz modrinth add better-leaves             # -> resourcepacks/better-leaves.pw.toml
packwiz curseforge add <slug>                  # CurseForge-only projects
packwiz update --all                           # pull newer versions of everything
```

Use packwiz rather than editing `.pw.toml` files by hand — it writes the pinned
version and hash and keeps `index.toml` consistent. `packwiz refresh` rebuilds the
index after any manual change.

Each `.pw.toml` is a *pointer*: a filename, a download URL and a hash. The jar or zip
itself never gets committed, which is what keeps the repo small and stays clear of
redistribution terms.

Set `side` in each `.pw.toml` to `both`, `client` or `server`. Client-only visual and
performance mods should be `client` so the server install stays clean.

## Shipping config files

Anything that isn't a download — configs, `options.txt`, keybinds, a server list —
is committed to the repo for real, laid out exactly as it sits in `.minecraft`:

```
packs/creative-preset/
  config/iris.properties      selects the shaderpack and enables it on first launch
  options.txt                 turns the resource pack on
```

Add the file, then `packwiz refresh` to pick it up. These land in `index.toml`
*without* `metafile = true`, since the content is right there rather than behind a URL.

Anything a player is expected to change afterward should be marked `preserve = true`
in `index.toml`, which every config file here is. Without it, the next pack update
overwrites their edits — including, for `options.txt`, every video setting they've
touched. With it, the file is written on first install and then left alone.

To pre-fill the in-game server list, drop a `servers.dat` in the pack root the same
way. It's NBT rather than text, so generate it from a working instance instead of
writing it by hand.

## Starting a new pack

```bash
cp -r packs/example packs/newpack
cd packs/newpack
$EDITOR pack.toml          # name, version, description; bump minecraft/fabric if needed
packwiz refresh
```

Then commit. The workflow globs every directory under `packs/`, so the new pack's
link is `.../releases/latest/download/newpack.mrpack` from its first build — no CI
changes needed.

## Installing packwiz locally

```bash
go install github.com/packwiz/packwiz@latest
```
