# /distill Command Usage

The `/distill` command works like any other commands on Distillery. For now, it only accepts one main input: an image URL:
- The input image can be either Distillery generated or anything external.
- The image URL must be a Discord URL, so make sure to upload the image to Discord first.

!!! tip
    When doing single image training, the quality of the input image is extremely important. The training is done at 768x resolution so ensure that the smaller side of the image is at least 768 pixels. Low noise, clear images, where the training subject is clearly visible, work much better.

### Example of /distill Command Launch
```plaintext
/distill prompt:https://cdn.discordapp.com/attachments/1132450797750337597/1200711915186442280/distillery_072e07ac-521f-4c4d-910b-f9e7494ba6ee.png
```
(Screenshot of the command launch goes here)

Once the command is sent, if no errors occur, you will see a confirmation message such as:
(Screenshot of the confirmation message goes here)

Finally, once the training is complete, you will see a confirmation message:
(Screenshot of the training completion message goes here)