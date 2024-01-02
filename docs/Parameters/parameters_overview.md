# Commands Overview

Parameters allows you to take the level of control of your image generation process to the next level. Parameters can be added to your prompt text in a specific format (typically `--parameter_name` format) and each of them does something to the image generation process. Make sure to try each of them to achieve the next level control!

This is a list of parameters available for `/serve` and `/serve-free` commands:

## Parameters:

!!! success "Prompt"
    - **Usage**: Simply start your command with the desired image description.
    - **Description**: Describes the kind of image you wish to generate. You don't need to prepend `--prompt`; the system assumes your first input as the prompt.

!!! info "Negative Prompt (`--neg`) [Learn More](negative_prompt/negative_prompt.md)"
    - **Description**: Indicates what you'd like to exclude from the image.
    - **Example**: `--neg light bulb`

!!! info "Seed (`--seed`): [Learn More](seed/seed.md)"
    - **Description**: Set a seed for your image. If unspecified, a random seed is selected. Useful for recalling a specific image or comparing parameter impacts. 
    - **Default Value**: `random number`
    - **Example**: `--seed 1991`

!!! info "(CFG) Classifier-Free Guidance (`--cfg`) [Learn More](cfg/cfg.md)"
    - **Default Value**: 6
    - **Description**: Dictates the model's adherence to your prompt. High values can impact image quality.
    - **Example**: `--cfg 8`

!!! info "Aspect Ratio (`--ar`) [Learn More](aspect_ratio/aspect_ratio.md)"
    - **Usage**: Specify as `x:y` (e.g., `1:1`, `9:16`).
    - **Description**: Changes the generation's aspect ratio. Available options vary depending on the model (SDXL or SD1.5).

!!! info "Denoise Strength (`--power`) [Learn More](denoise/denoise.md)"
    - **Default Value**: 0.3
    - **Description**: Adjusts denoise strength during upscaling. High values can introduce artifacts in images.

!!! info "Model (`--model`)"
    - **Default Value**: 'cosmopolitan'
    - **Options**: 'sdxl', 'vodka', 'screwdriver', 'mohawk', 'bloodymary'
    - **Description**: Chooses the model for image generation. Note that mohawk is SDXL custom model and SDXL workflows are applied

!!! info "LORAs (Low-Rank Adaptation) (`--lora`) [Learn More](lora/lora.md)"
    - **Description**: Appends an optional model for enhanced generation. For 'bloodymary', 'vodka', or 'screwdriver', there are dozens of LORAs available. SDXL currently supports 'nurlens'. See all othe LoRAs available via `/command-infos` and [here](lora/lora.md).

!!! info "Control Image (`--control`)"
    - **Usage**: Provide a Discord-hosted image URL.
    - **Description**: Constrains image generation based on the outlines of the provided image. Can be used with `--image`.

!!! info "Image to image (`--image`) [Learn More](img2img/img2img.md)" 
    - **Usage**: Provide a Discord-hosted image URL.
    - **Description**: Uses the specified image as a starting point for generation.

!!! info "Inpainting (`--inpaint`) [Learn More](inpaint/inpaint.md)" 
    - **Usage**: Provide a Discord-hosted image URL that contains masked area in alpha channel.
    - **Description**: Edit the image using a mask. Generation will happen only on the masked area
    - **Note**: Generate masks using 3d party tools or with /makemask command in Distillery. See details in Learn more.

!!! info "LLM: Large Language Model Assistants (`--llm`) [Learn More](llm/llm.md)" 
    - **Usage**: Transform your simple prompts into more interesting versions
    - **Description**: Fine-tuned LLMs are applied to user prompts to alter them in various ways

!!! info "IP Adapter (`--adapt`) [Learn More](adapt/adapt.md)"
    - **Description**: The `--adapt` parameter, allows user to prompt Stable Diffusion with the image input. It is a powerful tool that can be used in a various workflows for style, charachter, or other levels of control.
    - **Usage**: Provide a Discord-hosted image URL. up to four IP Adapters can be used per generation: `--adapt`, `--adapt2`, `--adapt3`, `--adapt4`
    - **Note**: Read documentation for the details, --adapt feature has a bit of learning curve.

!!! info "Sharpen Tool (`--sharpen`) [Learn More](sharpen/sharpen.md)" 
    - **Usage**: Makes images 'sharper', users can adjust the amount applied to images
    - **Description**: Post-processing tool that improves image aesthetics.

!!! info "Sampler Selection (`--sampler`) [Learn More](sampler/sampler.md)" 
    - **Usage**: Choose between legacy and LCM samplers "lcm", "legacy"
    - **Description**: Allow selection of the sampler.

!!! info "Raw (`--raw`) [Learn More](raw/raw.md)" 
    - **Usage**: add --raw parameter to the prompt to disable additional processing
    - **Description**: For generations that require higher level of control.

!!! info "Upscale Method (`--upscalemethod`) [Learn More](upscale_method/upscale_method.md)" 
    - **Usage**: Allows selecting which upscale method will be used: "legacy", "direct", "none"
    - **Description**: Impacts image quality and generation time

