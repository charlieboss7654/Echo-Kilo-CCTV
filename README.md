# EKS CCTV

Lightweight, CCTV Script for FiveM using ox_lib + ox_target.
Players can stand at configured security desks and use a third-eye option to view live CCTV!

## Features

* Multiple security desks, each with its own camera list
* Clean on-screen overlay: camera title + server timestamp
* Pan / Tilt / Zoom with configurable yaw limits (no endless spinning)
* Hard input lock while viewing (no Q crouch/cover, no movement)
* Next camera keybind (default N)
* Third-eye integration via ox_target
* Simple config and minimal performance impact


## Requirements

* ox_lib
* ox_target (if using third-eye)
* Recommended: OneSync enabled


## Installation

1. Place the resource folder (e.g. `EKS_CCTV`) in your `resources/`.

2. Add to `server.cfg` (ensure order):
   
   ensure ox_lib
   ensure ox_target
   ensure EKS_CCTV

3. Adjust `config.lua` (desks, cameras, yaw limit, text strings).


## Controls (default)

* Arrow keys > Pan/Tilt
* Q / E > Zoom in/out
* N > Next camera
* Backspace > Exit

> Player inputs are fully locked while viewing; only the above controls are read.


## Quick Config Notes

* Add desks with a `coords`/`radius` and a `cameras` list.
* Each camera supports `coords`, `rot`, optional `heading` (base yaw for clamping), and `fov`.
* Overlay strings and keycodes are customizable in `config.lua`.
* Set `UseTarget = true` to enable third-eye at desk coordinates.


## Troubleshooting

* Third-eye option not appearing

  * `UseTarget = true`, `ox_target` is started, and your desk `coords`/`radius` cover your position.

* Can't pan/zoom/next

  * Confirm your keycodes match your bindings; verify focus isn�t stolen by other UIs.

## Support

- Need help or want to share feedback?
   Discord: https://discord.gg/ePMrJPukBW



## Credits & License

* Created by Cowboy @ Echo Kilo Studios
* Uses ox_lib and ox_target by Overextended.
* Ripping code from this script is stricly prohibitted - If caught you will face blacklist!
