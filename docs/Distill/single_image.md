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

## How Does it Work

In this section, let's go through a step-by-step description of what happens once the user sends the /distill command:

1. **User Sends Request**: The user sends a /distill `<img_url>` request.
2. **LoRA Name Assignment**: As soon as the request is received, in the backend, a LoRA name is assigned to this request. It's a unique name composed of two rare tokens for Stable Diffusion.
3. **Confirmation Message**: At this point, the user receives back the confirmation that training will happen, along with the future LoRA name mentioned in point #2.
4. **Image Processing**: The image received from the user is renamed as `<LoRA_Name>.png` and saved in the backend. This file will stay there and can be referenced in different parameters, for example, `--adapt <LoRA_Name>.png`.
5. **Captioning the Image**: The uploaded image is being captioned using visual large language models, optimized for human portraits.
6. **Regularization Image Selection**: We use regularization images when training. At this step, each image is classified as either man, woman, or a person and 200 corresponding high-quality photographs are used as the regularization dataset.
7. **LoRA Training**: Everything is ready for actual LoRA training to start. We train our LoRAs on top of Distillery's Cosmopolitan SD 1.5 model. This means LoRAs won't be usable for SDXL models.
8. **Flip Augmentation**: To increase variability, the original image is mirrored, effectively 'doubling' the dataset. However, this can introduce problems in certain trainings for non-centered objects.
9. **Training Completion**: Once the training is done, the trained LoRA checkpoint is saved in the system, and the user receives a notification that it has been successfully distilled.

From here, users are able to use and manage the LoRAs they just distilled.

