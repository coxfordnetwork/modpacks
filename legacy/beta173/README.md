# beta173 — Minecraft Beta 1.7.3 (`beta.coxford.net`)

This one lives outside `packs/` on purpose. Everything the modern packs rely on —
Modrinth, Fabric, a `mods/` folder, `.mrpack` — postdates Beta 1.7.3 by years. Mods
of that era are patched *into* `minecraft.jar`, and the `.mrpack` format has no
concept of a jar mod, so there is no single-link install for this server. Client
setup is four clicks in Prism, done once.

What *is* config-managed here is the server: which build, which plugins, which
permissions.

## The stack

| Piece | What it does |
| --- | --- |
| [Project Poseidon](https://github.com/retromcorg/Project-Poseidon) | Server. CraftBukkit CB1060 fork for b1.7.3 — dupe fixes, crash fixes, UUID support. Runs era Bukkit plugins. |
| [BetaFix](https://github.com/tweska/BetaFix) | Client jar mod (MIT). Restores authentication, **skins and capes** without a third-party proxy. |

Skins are the reason both halves are needed. The b1.7.3 client fetched skins from a
Mojang endpoint that has been dead for a decade; BetaFix repoints it at the modern
API. Poseidon handles the server end of login so `online-mode` can stay on and
players are real accounts rather than anyone typing any username.

## Client setup

Prism lists the beta versions natively, so the vanilla side needs no help:

1. Add Instance → **Custom**, filter the version list to Beta, pick **b1.7.3**.
2. Edit Instance → **Add to Minecraft.jar**.
3. Select `BetaFix.zip` from the [latest BetaFix release](https://github.com/tweska/BetaFix/releases).
4. Launch once to confirm your skin renders.

That's the whole thing — no pack to maintain, no release to cut. If we ever want it
to be one link, the move is to build the instance once, export it from Prism, and
attach the zip to a release by hand; BetaFix is MIT so bundling it is fine, and Prism
downloads the vanilla b1.7.3 jar itself, so no Mojang binary ends up in the repo.

## Moderator abilities

**Beta 1.7.3 has no creative mode.** Creative arrived in Beta 1.8, three months
later. There is no gamemode to flip, so moderator powers come entirely from
server-side plugins:

| Plugin | Gives you |
| --- | --- |
| WorldEdit | The real one — `//set`, `//copy`, `//brush`, selections, undo |
| CommandBook | `/give`, `/tp`, `/god`, `/item`, time and weather |
| WorldGuard | Region protection, so the build server isn't griefable |
| Essentials + GroupManager | Permissions groups, homes, warps |

Pin exact versions in `server/plugins.md` as we settle them.

Two caveats worth knowing before promising anything:

**Flight.** The anti-fly kick in this era is server-side and predates the
`allow-flight` handling later versions grew. Check what the Poseidon jar writes into
`server.properties` on first run rather than assuming a key exists. If free-fly for
moderators turns out not to be grantable server-side, it needs an era client mod on
your instance alone — which is fine, since it only affects you.

**Sourcing plugins.** dev.bukkit.org links from 2011 are mostly dead. The
[BukkitMCBeta173 archive](https://archive.org/details/BukkitMCBeta173) on the Internet
Archive has ~50 of them including all four above. Mirror whatever we pick into this
directory or a release so the server doesn't depend on archive.org staying up.

## Networking

**No SRV records.** SRV lookup came to the Java client long after b1.7.3, so
`beta.coxford.net` has to be a plain A record pointing at the box, and the port has to
be one the client can reach directly.

Since 25565 is presumably already taken on that machine, players will type
`beta.coxford.net:PORT` with the port visible. Worth putting the full string on the
site verbatim rather than just the hostname — a b1.7.3 player who types the bare
hostname gets a connection failure with no hint as to why.

Also: a Cloudflare tunnel won't carry this. Minecraft is raw TCP, not HTTP, so it
needs a direct forward the way the other servers do.
