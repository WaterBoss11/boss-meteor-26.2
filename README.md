# Boss's Meteor 26.2

**A rebranded fork of [Meteor Client](https://github.com/MeteorDevelopment/meteor-client)** by MeteorDevelopment, built for **Minecraft 26.2** ("Chaos Cubed").

> ⚠️ **Pre-release quality.** This fork is built on **unmerged upstream PR [#6439 — "26.2 update"](https://github.com/MeteorDevelopment/meteor-client/pull/6439)**, which adds Minecraft 26.2 support to Meteor Client. Its author has flagged it as pre-release quality with possible runtime bugs. Use accordingly, and expect this fork to be superseded once MeteorDevelopment ships official 26.2 support.

## What this is

- All mod functionality is **Meteor Client**, unchanged — full credit to [MeteorDevelopment](https://github.com/MeteorDevelopment) and the Meteor contributors.
- The Minecraft 26.2 port is the work of [**Big-Iron-Cheems**](https://github.com/Big-Iron-Cheems), author of [upstream PR #6439](https://github.com/MeteorDevelopment/meteor-client/pull/6439); this fork is built from that PR's head.
- This fork exists only to provide a working 26.2 build ahead of an official Meteor release.

## Our changes on top of PR #6439

1. **Build fix — TerraformersMC Maven URL** (`build.gradle.kts`): the TerraformersMC repository moved its artifacts under a `/releases` path; the old root URL returns 404, which broke resolution of the ModMenu dependency. This fork appends `/releases` to the repository URL. This is the only functional change.
2. Cosmetic rebrand: mod display name (`fabric.mod.json` → "Boss's Meteor 26.2") and jar base name (`gradle.properties` → `boss-meteor`). The mod **id** remains `meteor-client`, and no package namespaces, mixin configs, asset paths, or copyright headers were altered.

## Building

Requires JDK 25.

```
./gradlew build
```

Output: `build/libs/boss-meteor-26.2-local.jar`

## License

[GPL-3.0](LICENSE) — the same license as upstream Meteor Client. The `LICENSE` file is the full, unmodified GPL-3.0 text as shipped by Meteor Client. All original copyright notices and source headers are preserved.
