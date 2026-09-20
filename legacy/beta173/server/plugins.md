# beta173 server manifest

Fill in the version and mirrored URL as each one is picked and tested against
Poseidon. Until a row is pinned, treat it as "not decided yet" rather than
"install whatever's newest" — almost every plugin from this era has later
versions that silently require a newer CraftBukkit API and fail at load.

## Server build

| | |
| --- | --- |
| Build | Project Poseidon |
| Version | _pin me_ |
| Source | https://github.com/retromcorg/Project-Poseidon/releases |
| Base | CraftBukkit CB1060 (Beta 1.7.3) |

## Plugins

| Plugin | Version | Purpose | Mirror |
| --- | --- | --- | --- |
| WorldEdit | _pin me_ | Terrain and build ops | |
| CommandBook | _pin me_ | `/give`, `/tp`, `/god`, time, weather | |
| WorldGuard | _pin me_ | Region protection | |
| Essentials | _pin me_ | Homes, warps, general utility | |
| GroupManager | _pin me_ | Permission groups | |

Era-appropriate builds of all of these are in the
[BukkitMCBeta173 archive](https://archive.org/details/BukkitMCBeta173). Mirror the
chosen jars somewhere we control — a release on this repo is fine — so the server
doesn't depend on archive.org.

## Permission groups

Sketch, to be replaced with the real GroupManager config once it's running:

- `default` — build and break, no commands beyond `/home` and `/spawn`
- `mod` — WorldEdit, CommandBook, WorldGuard region editing
- `admin` — everything, plus plugin reload

## Checklist before opening

- [ ] `online-mode=true` confirmed in the generated `server.properties`
- [ ] Skins render with BetaFix on a clean client instance
- [ ] Port chosen and forwarded; `beta.coxford.net` A record points at the box
- [ ] Full `host:port` string published on the site
- [ ] Spawn region protected with WorldGuard
- [ ] World backed up on the same schedule as the other servers
