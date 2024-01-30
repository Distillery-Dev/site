## Available Distillery Commands:

!!! success "Serve (`/serve`) [Learn More](serve/serve.md)"
    - **Usage**: type /serve followed by text prompt and additional parameters
    - **Description**: The main command at Distillery for generating images from Text. 
    - **Note**: For free version use `/serve-free`

!!! info "Zoomout (`/zoomout`) [Learn More](zoomout/zoomout.md)"
    - **Description**: Allows to zoomout and thus extend previously generated image
    - **Usage**: type /zoomout followed by discord url of the target image and thne add optional additional parameters
    - **Note**: For free version use `/zoomout-free`

!!! info "Upscale (`/upscale`) [Learn More](upscale/upscale.md)"
    - **Description**: Allows to upscale images that were previously generated on Distillery
    - **Usage**: type /upscale followed by discord url of the target image and then add optional additional parameters
    - **Note**: For free version use `/upscale-free`

!!! info "Check Image Metadata (`/checkmetadata`) [Learn More](checkmetadata/checkmetadata.md)"
    - **Description**: Check the metadata (details how image was generated of) images that were previously generated on Distillery
    - **Usage**: type /checkmetadata followed by discord url of the target image. The command doesn't accept any additional parameters
    - **Note**: The same command works for both free and paid users

!!! info "Command Infos in Discord (`/command-infos`) [Learn More](command_infos/command_infos.md)"
    - **Description**: A simple command to view information about Distillery commands on Discord.
    - **Usage**: type /command-infos

!!! info "User Stats (`/user-stats`) [Learn More](user_stats/user_stats.md)"
    - **Description**: A simple command to view your user level information on user status, credits, usage, available LoRAs, and so on
    - **Usage**: type /user-stats

!!! info "Manage Your LoRAs (`/manage-lora`) [Learn More](../Distill/manage_loras.md)"
    - **Description**: A command that allows you to view and update details for LoRAs available under your user.
    - **Usage**: type /manage-lora <LoRA Name>

!!! info "Suggest Prompt (`/suggest`) [Learn More](suggest/suggest.md)"
    - **Description**: Transforms your text prompt into an alternative version for variations and quality improvement
    - **Usage**: type /suggest followed by your prompt text that will be transformed into a new version. Additional parameter --llm allows selection of LLM model. For now only `--llm crazy` is available

!!! info "Create Image Mask (`/makemask`) [Learn More](makemask/makemask.md)"
    - **Description**: Create mask in alpha channel of the image. The generated mask can be used for inpainting (and other future features) as an input.
    - **Usage**: See Learn More for the detailed explanation on how to generate masks. Type /makemask followed by Discord URL of the image to get started.
    - **Note**: The command also accepts images that were not generated in Distillery.

!!! info "Distill LoRA (`/distill`) [Learn More](../Distill/distill_overview.md)"
    - **Description**: A command that allows you to train your own LoRAs. See details via the link
    - **Usage**: type /distill <img_url>