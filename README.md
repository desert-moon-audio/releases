# Desert Moon Audio - Releases

Public release channel for the Desert Moon Audio plugin line.

- `manifest.json` is read once a day by every installed DMA plugin. When it
  lists a newer version than the one running, the plugin shows a small
  "UPDATE AVAILABLE" notice that links to the download here.
- Installer `.pkg` files are attached to the tagged releases of this
  repository (one tag per product, e.g. `dino-roar-v1.0.1`).

## Cutting a release

1. Bump `project(... VERSION x.y.z)` in the plugin's CMakeLists.txt.
2. Run `Tools/make_installer.sh` with the iLok plugged in.
3. `gh release create <product>-vx.y.z <the .pkg> --repo desert-moon-audio/releases --title "<Product> x.y.z"`
4. Update that product's entry in `manifest.json` (version + url) and push.

Installed plugins pick the change up within a day.
