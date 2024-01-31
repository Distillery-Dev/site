# Single Image Training Overview

## Overview

Single Image Training is the first and simplest implementation of LoRA Training via the `/distill` function in Distillery. As the name suggests, it enables training a LoRA with just a single image.

!!! important
    Training a LoRA with a single image has both strengths and weaknesses. While it simplifies the process and offers clear data lineage, the limited data can restrict flexibility. This may require multiple attempts to fine-tune the prompt and parameters. It's most effective for specific use-cases.

The current implementation is optimized for human faces, particularly for preserving characters created in Distillery or other AI generators. It works best with portrait-type images, real portrait photos of humans, paintings, and similar mediums.

!!! warning
    The input image's quality is crucial, as the training relies on minimal data. High resolution, clarity, and low noise in portrait-style square images produce the best results.

Other applications, such as training styles, animals, creatures, items, etc., are in an experimental stage. Expect variability in the quality of the results for these use cases. 

!!! suggestion
    For a deeper understanding of the process and its limitations, refer to the "How does it work" section below.

## Case Study

[WIP] In this section, we will cover a step-by-step example from training a LoRA to applying it in various scenarios, with different prompting styles and parameter usage.

## How does it work

[WIP blank for now]
