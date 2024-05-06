# Zoomout Overview

`/zoomout` is a feature in Distillery that allows users to expand their generated images in all four directions. It works by adding an empty frame around the original image and then running the Stable Diffusion process to fill in that frame. This feature is only applicable to Distillery-generated images.

Please note that the implementation of `/zoomout` differs significantly between SDXL and SD1.5-based models, affecting the quality and behavior of the output.

!!! note "--lazy zoomouts"
    The current version of `/zoomout` may tend to produce less detailed expansions. This can be mitigated by adjusting the `--power` and `--cfg` parameters.

To use `/zoomout`, you will need a Distillery-generated image url that should be provided to the `/zoomout` command.

## Available Additional Parameters for /zoomout:

| Parameter             | Link to Docs (WIP, to be added)                                  | Simple Overview                    |
|-----------------------|------------------------------------------------------------------|------------------------------------|
| `--neg`               | [Negative Prompts](../../Parameters/negative_prompt/negative_prompt.md)  | Add Negative Prompt `--neg night`  |
| `--seed`              | [Seed](../../Parameters/seed/seed.md)                                   | Control Image Generation Seed `--seed 123` |
| `--cfg`               | [CFG](../../Parameters/cfg/cfg.md)                                      | Choose desired CFG value `--cfg 4.5` |
| `--power`             | [Denoise](../../Parameters/denoise/denoise.md)                              | Adjust Denoise Strength `--power 0.2` |
| `--sharpen`           | [Sharpen](../../Parameters/sharpen/sharpen.md)                          | Adjust sharpening value `--sharpen 0` |
| `--inpaintcontrol`    | [Inpainting Control](../../Parameters/inpaint/inpaint.md) | SD15 only, adjust strength of controlnet used for inpainting `--inpaintcontrol 0` |
| `--refinerpass`       | [Refiner Pass](../../Parameters/upscale_method/upscale_method.md)             | SDXL only, choose portion of generation to be done with refiner model `--refinerpass 0.5` |
| `--zoomoutfactor`     | See details on this page      | Control how much the image zooms out `--zoomoutfactor 0.7` |

