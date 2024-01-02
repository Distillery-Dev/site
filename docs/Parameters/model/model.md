# Models Overview

`--model` is a parameter that allows you to select the model which will be used for image generation. In this context, a model refers to a version of Stable Diffusion that Distillery is running. As of now, Distillery runs models that are either based on Stable Diffusion 1.5 or Stable Diffusion XL (SDXL).

It's important to understand which model is which, as the workflows, applicable LoRAs, and details can vary between the two. Here's a look at the available models:

## Available Models

| Model Name   | Model Type | Link                                                           | Description                                                                                           |
|--------------|------------|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Cosmopolitan | SD 1.5     | [Cosmopolitan](https://civitai.com/models/194647)              | Default model on Distillery. Our own fine-tune                                                        |
| Vodka        | SD 1.5     | [Vodka](https://civitai.com/models/61086?modelVersionId=105782)| Custom in-house fine-tuned 1.5 model that is a pre-mix version of Cosmopolitan. Useful in some edge cases |
| Screwdriver  | SD 1.5     | No Link                                                       | In-house mix that is mostly deprecated.                                                               |
| SDXL         | SDXL       | [SDXL](https://huggingface.co/docs/diffusers/using-diffusers/sdxl)| SDXL Official Model                                                                                  |
| Mohawk       | SDXL       | [Mohawk](https://civitai.com/models/144952?modelVersionId=207419)| 3rd party fine-tune of SDXL model, authored by [Aurety](https://civitai.com/user/Aurety). Powerful but opinionated model. |

Each model has its own characteristics, capabilities, and limitations. It's recommended to try different models and see which one suits your needs best.
