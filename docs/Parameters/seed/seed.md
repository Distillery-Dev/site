## The `--seed` Parameter for Controlled Iterations

Using the `--seed` parameter can greatly assist in iterative experimentation, allowing users to observe the effects of modifying prompts and other parameters on their image generations.

!!! warning "Important Note"
    If you aim to continually generate varied images, simply exclude the `--seed` parameter from your prompts.

### Starting with a Basic Example

Let's begin with our previous example, but this time we'll incorporate a specific seed number.

```plaintext
/serve-free prompt: old bartender in the bar with a long beard --seed 123
```

**On Discord, your command would appear as:**  
![Image 1](1_seed_example_1.png)

**This is the first image generated using the prompt:**  
![Image 2](2_seed_result_1.png){: width="500px" }

If you were to generate this exact prompt with this seed number multiple times, each time you will get exact same output. This is what allows the itterative control.

### Adjusting the Prompt

Now, let's slightly tweak our prompt to understand its effect on the generated images. For this exercise, we'll prepend the phrase "oil painting of" to our original prompt.

```plaintext
/serve-free prompt: oil painting of old bartender in the bar with a long beard --seed 123
```
![Image 3](3_seed_example_2.png)

**Observing the new results:**  
![Image 4](4_seed_result_2.png){: width="500px" }

As can be clearly seen, the modified image now resembles an oil painting.

!!! tip "Pro Tip"
    The `--seed` command can be paired with any combination of other parameters for varied effects.

!!! info "How does this work?"
    Stable Diffusion begins its image generation process from a random noise. By setting a specific `seed` number, you ensure that the starting noise remains consistent every time, leading to reproducible results.
