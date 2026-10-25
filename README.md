# Stockbridge cabin

The published pages for a 14' x 20' cabin with a loft in Stockbridge, Vermont. This repo is a GitHub Pages site and holds
only generated HTML. Live at https://zannahpierce-pico.github.io/stockbridge-cabin/

| Page | What it is |
|---|---|
| [index.html](https://zannahpierce-pico.github.io/stockbridge-cabin/) | 3D model of the cabin, inside and out, with the furniture, cabinet wall, deck and cable runs |
| [electrical-plan.html](https://zannahpierce-pico.github.io/stockbridge-cabin/electrical-plan.html) | 2D electrical plan: outlets, switches, lights, circuits, the materials list with Home Depot links, and the wiring research |
| [cabinet-wall.html](https://zannahpierce-pico.github.io/stockbridge-cabin/cabinet-wall.html) | The built-in cabinet wall between the living room and the future bath |
| [building-notes.html](https://zannahpierce-pico.github.io/stockbridge-cabin/building-notes.html) | Notes on the build |

The pages are public but not indexed. Each page opens in guest view; add `?admin` to the address once to turn on the owner
controls in that browser, and `?admin=off` to turn them off again.

## Do not edit here

Nothing in this repo is edited by hand. The source lives in the private repo
[zannahpierce-pico/building-models](https://github.com/zannahpierce-pico/building-models), under `buildings/stockbridge-cabin/`:

- `openings.py`: windows and doors as built
- `layout.py`: everything inside, including the outlets, switches and lights
- `make_plan.py` and `plan_page.html`: the electrical plan page
- `build3d.py` and `viewer.html`: the 3D model
- `SHOPPING.md`, `WIRING-NOTES.md`, `HOME-DEPOT.md`: the notes and lists behind the pages

To change a page, edit the source there, rebuild (`python3 make_plan.py out`, `python3 build3d.py out`, and so on), then run
`publish_site.sh` from the root of building-models. That script copies the built pages into this repo, commits and pushes, and
GitHub Pages picks the change up within a minute or two. Anything added to this repo by hand will be left alone by the script
but will not be part of the build.
