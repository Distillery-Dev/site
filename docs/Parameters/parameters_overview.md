# Commands Overview

Parameters allows you to take the level of control of your image generation process to the next level. Parameters can be added to your prompt text in a specific format (typically `--parameter_name` format) and each of them does something to the image generation process. Make sure to try each of them to achieve the next level control!

This is a list of parameters available for `/serve` and `/serve-free` commands:

## Parameters:

!!! success "Prompt"
    - **Usage**: Simply start your command with the desired image description.
    - **Description**: Describes the kind of image you wish to generate. You don't need to prepend `--prompt`; the system assumes your first input as the prompt.

!!! info "Seed (`--seed`): [Learn More](/path/to/your/page/)"
    - **Description**: Set a seed for your image. If unspecified, a random seed is selected. Useful for recalling a specific image or comparing parameter impacts. 
    - **Default Value**: `random number`
    - **Example**: `--seed 1991`

!!! info "Negative Prompt (`--neg`)"
    - **Description**: Indicates what you'd like to exclude from the image.

!!! info "Classifier-Free Guidance (`--cfg`)"
    - **Default Value**: 6
    - **Description**: Dictates the model's adherence to your prompt. High values can impact image quality.

!!! info "Aspect Ratio (`--ar`)"
    - **Usage**: Specify as `x:y` (e.g., `1:1`, `9:16`).
    - **Description**: Changes the generation's aspect ratio. Available options vary depending on the model (SDXL or SD1.5).

!!! info "Denoise Strength (`--power`)"
    - **Default Value**: 0.3
    - **Description**: Adjusts denoise strength during upscaling. High values can introduce artifacts in images.

!!! info "Inspiration Image (`--image`)"
    - **Usage**: Provide a Discord-hosted image URL.
    - **Description**: Uses the specified image as a starting point for generation.

!!! info "Control Image (`--control`)"
    - **Usage**: Provide a Discord-hosted image URL.
    - **Description**: Constrains image generation based on the outlines of the provided image. Can be used with `--image`.

!!! info "Model (`--model`)"
    - **Default Value**: 'bloodymary'
    - **Options**: 'sdxl', 'vodka', 'screwdriver'
    - **Description**: Chooses the model for image generation.

!!! info "Low-Rank Adaptation (`--lora`)"
    - **Description**: Appends an optional model for enhanced generation. For 'bloodymary', 'vodka', or 'screwdriver', over 10 LORAs are available. SDXL currently supports 'nurlens'. More LORA info is available via `/command-infos`.

