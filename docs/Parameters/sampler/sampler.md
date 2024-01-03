# Sampler

The `--sampler` parameter allows users to select the sampling methodology used for image generation. Sampling, in essence, is the part of the process where Stable Diffusion creates images, and there are various approaches to how this can be done.

The main reason for exposing `--sampler` selection in Distillery is the introduction of the LCM sampling method that significantly reduces generation times. See below for the details.

Currently, `--sampler` has two allowed values: `--sampler legacy` (default) or `--sampler lcm`.

### Sampler Legacy
The `sampler legacy` refers to UniPC sampler in the case of SD 1.5 models (see [UniPC](https://github.com/wl-zhao/UniPC)) or EulerAncestral sampler in the case of SDXL based models (see [EulerAncestral](https://huggingface.co/docs/diffusers/api/schedulers/euler_ancestral)).

### LCM Overview
*Documentation Coming Soon*