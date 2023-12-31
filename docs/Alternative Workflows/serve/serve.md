# Serve Overview

## Available Additional Parameters:

| Parameter             | Link to Docs (WIP, to be added)                                  | Simple Overview                    |
|-----------------------|-----------------------------------------------|------------------------------------|
| `--neg`               | [Negative Prompts](../../Parameters/negative_prompt/negative_prompt.md)  | Add Negative Prompt `--neg night`                   |
| `--seed`              | [Seed](../../Parameters/seed/seed.md)               | Control Image Generation Seed `--seed 123`                   |
| `--cfg`               | [CFG](../../Parameters/cfg/cfg.md)                 | Choose desired CFG value `--cfg 4.5`                   |
| `--ar`                | [AR](../../Parameters/aspect_ratio/aspect_ratio.md)                   | Choose image aspect ratio `--ar 16:9`                   |
| `--power`             | [Denoise](../../Parameters/denoise/denoise.md)             | Adjust hiresfix strength `--power 0.2`                   |
| `--model`             | [Models](../../Parameters/model/model.md)             | Choose which model to use `--model sdxl`                   |
| `--lora`              | [LORAs](../../Parameters/lora/lora.md)               | Apply up to 5 LoRAs to generation `--lora realism`                   |
| `--control`           | [Controlnet](../../Parameters/control/control.md)         | Guide image generation using controlnet input `--control <img url>`                   |
| `--image`             | [Image2image](../../Parameters/img2img/img2img.md)             | Use input image as a starting point `--image <img url>`                   |
| `--inpaint`           | [Inpainting](../../Parameters/inpaint/inpaint.md)         | Inpaint/change only the masked area of the image `--inpaint <img with mask url>`                   |
| `--inpaintmaskfeather`| [Inpainting](../../Parameters/inpaint/inpaint.md) | Adjust feathering value when inpainting `--inpaintmaskfeather 2`               |
| `--inpaintmaskgrow`   | [Inpainting](../../Parameters/inpaint/inpaint.md)     | Adjust mask size when inpainting `--inpaintmaskgrow 20`               |
| `--llm`               | [LLM](../../Parameters/llm/llm.md)                 | Modify your prompt with the help of LLMs `--llm crazy`                   |
| `--lcmweight`         | [Sampler](../../Parameters/sampler/sampler.md)     | Only applicable when LCM sampler is used                   |
| `--adapt, --adapt2, --adapt3, --adapt4` | [IPAdapters](../../Parameters/adapt/adapt.md) | use IPAdapters to prompt with images `--adapt <img url>`          |
| `--adaptweight`       | [IPAdapters](../../Parameters/adapt/adapt.md) | Adjust IPAdapter strength `--adaptweight 0.3`                   |
| `--sharpen`           | [Sharpen](../../Parameters/sharpen/sharpen.md)         | Adjust sharpening value `--sharpen 0`                   |
| `--sampler`           | [Sampler](../../Parameters/sampler/sampler.md)         | Change sampling method `--sampler lcm`                   |
| `--raw`               | [RAW](../../Parameters/raw/raw.md)                 | Disable some of the added processing for more control `--raw`                   |
| `--force-model`       | [Models](../../Parameters/model/model.md)  | Forces inpaint to work with the selected model (vs using inpainting-finetuned ones)    |
| `--controlweight`     | [Controlnet](../../Parameters/control/control.md) | Adjust strength of controlnets `--controlweight 0.3`               |
| `--inpaintcontrol`    | [Inpainting](../../Parameters/inpaint/inpaint.md) | SD15 only, adjust strength of controlnet used for inpainting `--inpaintcontrol 0`               |
| `--imagedenoise`      | [Image2image](../../Parameters/img2img/img2img.md)    | Adjust the portion of initial image to keep for image2image `--imagedenoise 0.8`               |
| `--upscalemethod`     | [Upscale](../../Parameters/upscale_method/upscale_method.md) | Choose the method to upscale or disable it. `--upscalemethod none`               |
| `--refinerpass`       | Refinerpass | SDXL only, choose portion of generation to be done with refiner model `--refinerpass 0.5`                   |
| `--cutoffweight`       | Cutoffweight | Adjust Cutoff weight `--cutoffweight 1.5`                   |

