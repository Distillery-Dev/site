# Zoomout Overview
*Detailed Documentation Coming Soon*

## Available Additional Parameters for /zoomout:

| Parameter             | Link to Docs (WIP, to be added)                                  | Simple Overview                    |
|-----------------------|------------------------------------------------------------------|------------------------------------|
| `--neg`               | [Negative Prompts](../../Parameters/negative_prompt/negative_prompt.md)  | Add Negative Prompt `--neg night`  |
| `--seed`              | [Seed](../../Parameters/seed/seed.md)                                   | Control Image Generation Seed `--seed 123` |
| `--cfg`               | [CFG](../../Parameters/cfg/cfg.md)                                      | Choose desired CFG value `--cfg 4.5` |
| `--power`             | [Denoise](../../Parameters/denoise/denoise.md)                              | Adjust Denoise Strength `--power 0.2` |
| `--adaptweight`       | [Adaptweight](../../Parameters/adapt/adapt.md)              | Adjust IPAdapter strength `--adaptweight 0.3` |
| `--sharpen`           | [Sharpen](../../Parameters/sharpen/sharpen.md)                          | Adjust sharpening value `--sharpen 0` |
| `--inpaintcontrol`    | [Inpainting Control](../../Parameters/inpaint/inpaint.md) | SD15 only, adjust strength of controlnet used for inpainting `--inpaintcontrol 0` |
| `--refinerpass`       | [Refiner Pass](../../Parameters/upscale_method/upscale_method.md)             | SDXL only, choose portion of generation to be done with refiner model `--refinerpass 0.5` |
| `--zoomoutfactor`     | See details on this page      | Control how much the image zooms out `--zoomoutfactor 0.7` |

