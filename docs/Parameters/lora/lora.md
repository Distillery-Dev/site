# LoRA (Low Rank Adaptation)

LoRA, or **Low Rank Adaptation**, is an optional model that can be appended to the generation. Each LoRA adds a small neural network to the original model, aiming to influence it towards its specific generative goal. By adding `--lora` followed by the name of the LoRA model to be used, you can add it to the generation. 

By default, no LoRAs are used unless specifically asked for by the user.

Up to 5 LoRAs can be used at any single time, but their individual influence is reduced by every additional LoRA model. This is automatically done by Distillery's backend in order to preserve the quality of the generative output, since too many LoRAs may generate additional noise in the final product.

!!! tip "How LoRAs actually work"
    A LoRA is controlled by two main parameters: its **weight**, which determines how strongly its influence must be on the original model's output, and its **activation keywords**, which are the words that must be used in order to let the LoRA know it must work. Distillery is handling the weight of the LoRA automatically, so the only thing the user must focus on is the generation prompt.

While the best LoRAs will always be the ones trained over the model that is invoked for the generation, most LoRAs can be ported from one model checkpoint to another of the same family (that is: SD1.5-based LoRAs work across most SD1.5 model checkpoints, and the same goes for SDXL). 

LoRAs are unique tools at our disposal in the generative art toolkit. Think of them as "cartridges" to the model checkpoints' "consoles".

## Loras for SD 1.5 models

The following LoRAs are available for our standard models (bloodymary, vodka and screwdriver):


| LoRA name  | Creator  | Description  | Activation words  | Available In                        |
|------------|----------|--------------|-------------------|-------------------------------------|
| ```realism``` | Distillery | Photorealistic and prompt-compliant generations | None | [Link](https://civitai.com/models/90467?modelVersionId=105772) |
| ```analog``` | [alenknight](https://civitai.com/user/alenknight)   | Analog photography | ```analog style``` | [Link](https://example.com/link2)|



## Practical Exploration

To understand CFG's impact, let's start with our familiar bartender example.

```plaintext
/serve-free prompt: old bartender in the bar with a long beard --seed 123
```

![Image 1](1_starting_image.png){: width="500px" }

With the original value being 6, let's see the effect of a lower CFG value of --cfg 3:

```plaintext
/serve-free prompt: old bartender in the bar with a long beard --seed 123 --cfg 3
```
![Image 2](2_cfg_3.png){: width="500px" }

Now, let's drastically increase the CFG value to --cfg 10:

```plaintext
/serve-free prompt: old bartender in the bar with a long beard --seed 123 --cfg 10
```
![Image 3](3_cfg_10.png){: width="500px" }

Notice the significant changes in the generated images. While the default might seem optimal for this simple example, remember that as you introduce more parameters and models, experimenting with CFG values can prove beneficial.


