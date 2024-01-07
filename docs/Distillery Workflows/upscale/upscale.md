# Upscale Overview

`/upscale` is the command that allows you to upscale images generated in Distillery. All images generated in Distillery using `/serve` commands are 1024x1024 pixels when using a 1:1 ratio, and the dimensions for other aspect ratios are adjusted such that the total pixel count stays close to that.

When using `/upscale`, the image dimensions are increased 2x, meaning the total pixel count is increased 4x.

To achieve this, images are first upscaled using traditional upscalers (as of today, it's [4x-UltraSharp](https://openmodeldb.info/models/4x-UltraSharp)) followed by a Stable Diffusion HiRes Fix pass. The latter is essentially Stable Diffusion regenerating small parts of the image with some amount of denoise strength while keeping all the original prompts, LoRAs, and other parameters used in the initial generation.

The base usage is very simple: type the `/upscale` command followed by a Discord image URL.

The HiRes Fix pass allows us to introduce a few additional controls over the upscaling process, including the `--power` parameter, which typically makes the difference between good and bad upscales.

### Basic Usage

Type `/upscale` command followed by the Discord URL of the image.

!!! tip "--power"
    HiRes Fix can add a lot of the desired details to the image but it can also lead to hallucinations and duplicated items on the image. When this happens, try lowering --power to the lower values (default is 0.3). You can typically find an optimal point that balances new details without too much undesired artifacts. 

## Available Additional Parameters for /upscale:

| Parameter            | Link to Docs (WIP, to be added)                                    | Simple Overview                     |
|----------------------|--------------------------------------------------------------------|-------------------------------------|
| `--neg`              | [Negative Prompts](../../Parameters/negative_prompt/negative_prompt.md)  | Add Negative Prompt `--negative_prompt night` |
| `--seed`             | [Seed](../../Parameters/seed/seed.md)                                     | Control Image Generation Seed `--seed 123` |
| `--cfg`              | [CFG](../../Parameters/cfg/cfg.md)                                        | Choose desired CFG value `--cfg 4.5` |
| `--power`            | [Denoise](../../Parameters/denoise/denoise.md)                                | Adjust Denoise Strength `--power 0.2` |
| `--sharpen`          | [Sharpen](../../Parameters/sharpen/sharpen.md)                            | Adjust sharpening value `--sharpen 0` |

