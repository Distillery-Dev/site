# CFG (Classifier-Free Guidance)

CFG, or **Classifier-Free Guidance**, provides a powerful way to optimize your image generation. It determines how strictly the model adheres to the provided text prompt. By adding `--cfg` followed by a desired number to your command, you can control its behavior. The default value is set at `--cfg 6`.

!!! tip "Recommended Range"
    Typically, a CFG value between 3 and 12 yields the most consistent results.

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