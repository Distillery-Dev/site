# Commands Overview

Get familiar with the parameters available for `/serve` and `/serve-free` commands to customize your image generation.

## Parameters:

- **Prompt**:
    - **Usage**: Simply start your command with the desired image description.
    - **Description**: Describes the kind of image you wish to generate. You don't need to prepend `--prompt`; the system assumes your first input as the prompt.

- **Negative Prompt (`--neg`)**:
    - **Description**: Indicates what you'd like to exclude from the image.

- **Seed (`--seed`)**:
    - **Description**: Set a seed for your image. If unspecified, a random seed is selected. Useful for recalling a specific image or comparing parameter impacts.

- **Classifier-Free Guidance (`--cfg`)**:
    - **Default Value**: 6
    - **Description**: Dictates the model's adherence to your prompt. High values can impact image quality.

- **Aspect Ratio (`--ar`)**:
    - **Usage**: Specify as `x:y` (e.g., `1:1`, `9:16`).
    - **Description**: Changes the generation's aspect ratio. Available options vary depending on the model (SDXL or SD1.5).

- **Denoise Strength (`--power`)**:
    - **Default Value**: 0.3
    - **Description**: Adjusts denoise strength during upscaling. High values can introduce artifacts in images.

- **Inspiration Image (`--image`)**:
    - **Usage**: Provide a Discord-hosted image URL.
    - **Description**: Uses the specified image as a starting point for generation.

- **Control Image (`--control`)**:
    - **Usage**: Provide a Discord-hosted image URL.
    - **Description**: Constrains image generation based on the outlines of the provided image. Can be used with `--image`.

- **Model (`--model`)**:
    - **Default Value**: 'bloodymary'
    - **Options**: 'sdxl', 'vodka', 'screwdriver'
    - **Description**: Chooses the model for image generation.

- **Low-Rank Adaptation (`--lora`)**:
    - **Description**: Appends an optional model for enhanced generation. For 'bloodymary', 'vodka', or 'screwdriver', over 10 LORAs are available. SDXL currently supports 'nurlens'. More LORA info is available via `/command-infos`.
