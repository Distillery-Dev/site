# Zoomout Overview

## Available Additional Parameters for /zoomout:

| Parameter             | Link to Docs (WIP, to be added)                                  | Simple Overview                    |
|-----------------------|------------------------------------------------------------------|------------------------------------|
| `--neg`               | [Negative Prompts](../../Parameters/negative_prompt/negative_prompt.md)  | Add Negative Prompt `--neg night`  |
| `--seed`              | [Seed](../../Parameters/seed/seed.md)                                   | Control Image Generation Seed `--seed 123` |
| `--cfg`               | [CFG](../../Parameters/cfg/cfg.md)                                      | Choose desired CFG value `--cfg 4.5` |
| `--power`             | [Denoise](../../Parameters/denoise/denoise.md)                              | Adjust Denoise Strength `--power 0.2` |
| `--adaptweight`       | [Adaptweight](../../Parameters/adapt/adapt.md)              | Adjust IPAdapter strength `--adaptweight 0.3` |
| `--sharpen`           | [Sharpen](../../Parameters/sharpen/sharpen.md)                          | Adjust sharpening value `--sharpen 0` |
| `--inpaintcontrol`    | [Inpainting Control](../../Parameters/inpaint/inpaint.md) | Adjust strength of controlnet used for inpainting `--inpaintcontrol 0` |
| `--upscalemethod`     | [Upscale Method](../../Parameters/upscale/upscale.md)       | Choose the method to upscale or disable it `--upscalemethod none` |
| `--refinerpass`       | [Refiner Pass](../../Parameters/upscale/upscale.md)             | SDXL only, choose portion of generation to be done with refiner model `--refinerpass 0.5` |
| `--zoomoutfactor`     | [Zoom Out Factor](../../Parameters/zoomout/zoomout.md)      | Control how much the image zooms out `--zoomoutfactor 2` |
