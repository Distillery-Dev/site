# LoRA (Low Rank Adaptation)

LoRA, or **Low Rank Adaptation**, is an optional model that can be appended to the generation. By adding `--lora` followed by the name of the LoRA model to be used, you can add it to the generation. By default, no LoRAs are used unless specifically asked for by the user.

Up to 5 LoRAs can be used at any single time, but their individual influence is reduced by every additional LoRA model. This is automatically done by Distillery's backend in order to preserve the quality of the generative output, since too many LoRAs may generate additional noise in the final product.

!!! tip "How LoRAs work"
    Each LoRA adds a small neural network to the original model, aiming to influence it towards its specific generative goal. A LoRA is controlled by two main parameters: its **weight**, which determines how strongly its influence must be on the original model's output, and its **activation keywords**, which are the words that must be used in order to let the LoRA know it must work. Distillery is handling the weight of the LoRA automatically, so the only thing the user must focus on is the generation prompt.

While a higher CFG value implies stricter adherence to the prompt, it doesn't guarantee improved image quality. In fact, after a certain threshold, the image quality can degrade. Therefore, it's not simply a matter of always using a higher value.

Moreover, the best CFG value often depends on the unique combination of prompts, models, and other parameters you're using. It's crucial to experiment to find the sweet spot for your specific generation.

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



| LoRA name  | Creator  | Description  | Activation words  | Available In                        |
|------------|----------|--------------|-------------------|-------------------------------------|
| Data 1     | Data 2   | Data 3       | Data 4            | [Data 5](https://example.com/link1) |
| Data 6     | Data 7   | Data 8       | Data 9            | [Data 10](https://example.com/link2)|

