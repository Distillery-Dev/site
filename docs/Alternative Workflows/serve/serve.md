# Serve Overview

## Available Additional Parameters:

| Parameter             | Link to Docs (WIP, to be added)                                  | Simple Overview                    |
|-----------------------|-----------------------------------------------|------------------------------------|
| `--neg`               | [Negative Prompts](Parameters/negative_prompt/negative_prompt.md)  | Add Negative Prompt `--neg night`                   |
| `--seed`              | [Seed](Parameters/seed/seed.md)               | Control Image Generation Seed `--seed 123`                   |
| `--cfg`               | [CFG](Parameters/cfg/cfg.md)                 | Choose desired CFG value `--cfg 4.5`                   |
| `--ar`                | [AR](Parameters/ar/ar.md)                   | Choose image aspect ratio `--ar 16:9`                   |
| `--power`             | [Denoise](Parameters/power/power.md)             | Adjust hiresfix strength `--power 0.2`                   |
| `--model`             | [Models](Parameters/model/model.md)             | Choose which model to use `--model sdxl`                   |
| `--lora`              | [LORAs](Parameters/lora/lora.md)               | Apply up to 5 LoRAs to generation `--lora realism`                   |
| `--control`           | [Controlnet](Parameters/control/control.md)         | Guide image generation using controlnet input `--control <img url>`                   |
| `--image`             | [Image2image](Parameters/image/image.md)             | Use input image as a starting point `--image <img url>`                   |
| `--inpaint`           | [Inpainting](Parameters/inpaint/inpaint.md)         | Inpaint/change only the masked area of the image `--inpaint <img with mask url>`                   |
| `--inpaintmaskfeather`| [Inpainting](Parameters/inpaint/inpaint.md) | Adjust feathering value when inpainting `--inpaintmaskfeather 2`               |
| `--inpaintmaskgrow`   | [Inpainting](Parameters/inpaint/inpaint.md)     | Adjust mask size when inpainting `--inpaintmaskgrow 20`               |
| `--llm`               | [LLM](Parameters/llm/llm.md)                 | Modify your prompt with the help of LLMs `--llm crazy`                   |
| `--lcmweight`         | [Sampler](Parameters/lcmweight/lcmweight.md)     | Only applicable when LCM sampler is used                   |
| `--adapt, --adapt2, --adapt3, --adapt4` | [IPAdapters](Parameters/adapt_series/adapt_series.md) | use IPAdapters to prompt with images `--adapt <img url>`          |
| `--adaptweight`       | [IPAdapters](Parameters/adaptweight/adaptweight.md) | Adjust IPAdapter strength `--adaptweight 0.3`                   |
| `--sharpen`           | [Sharpen](Parameters/sharpen/sharpen.md)         | Adjust sharpening value `--sharpen 0`                   |
| `--sampler`           | [Sampler](Parameters/sampler/sampler.md)         | Change sampling method `--sampler lcm`                   |
| `--raw`               | [RAW](Parameters/raw/raw.md)                 | Disable some of the added processing for more control `--raw`                   |
| `--force-model`       | [Link](Parameters/force-model/force-model.md) | what's this?                   |
| `--controlweight`     | [Controlnet](Parameters/control/control.md) | Adjust strength of controlnets `--controlweight 0.3`               |
| `--inpaintcontrol`    | [Inpainting](Parameters/inpaint/inpaint.md) | Adjust strength of controlnet used for inpainting `--inpaintcontrol 0`               |
| `--imagedenoise`      | [Image2image](Parameters/image/image.md)   | Adjust the portion of initial image to keep for image2image `--imagedenoise 0.8`               |
| `--upscalemethod`     | [Upscale](Parameters/upscalemethod/upscalemethod.md) | Choose the method to upscale or disable it. `--upscalemethod none`               |
| `--refinerpass`       | [Link](Parameters/refinerpass/refinerpass.md) | SDXL only, choose portion of generation to be done with refiner model `--refinerpass 0.5`                   |

