# Stable Diffusion with Nix

Quickly get up and running using Stable Diffusion with Nix flakes.
Cloned from [collinarnett/stable-diffusion-nix](https://github.com/collinarnett/stable-diffusion-nix).

## Requirements

* [Nix](https://nixos.org/download.html)
* Nvidia GPU (3.2GB VRAM)
* x86_64 Linux

## Setup

1. Enable flakes by editing either `~/.config/nix/nix.conf` or `/etc/nix/nix.conf` and add
```
experimental-features = nix-command flakes
```

2. Use `nix run --impure` to spawn a Jupyter Lab instance. The `--impure` flag allows nixGL to find your Nvidia drivers on non-nixos systems.

3. Update `stable-diff.cfg` with HuggingFace token and make sure to accept the [License Agreement](https://huggingface.co/CompVis/stable-diffusion-v1-4) for Stable Diffusion.

4. Update `stable-diff.cfg` with output directory

5. Execute the cells in `stable-diff.ipynb` to generate images.
