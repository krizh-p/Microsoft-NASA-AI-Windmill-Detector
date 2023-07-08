# SAM Automatic Mask Generator for Windmill Detection

This code demonstrates how to automatically generate object masks using SAM (Segment Anything Model) to identify windmills in images. SAM is a model developed by Meta Platforms, Inc. and its affiliates that can efficiently process prompts to generate masks for an entire image. This method was used to generate the SA-1B dataset.

The SamAutomaticMaskGenerator class implements this capability by sampling single-point input prompts in a grid over the image. From each of these prompts, SAM can predict multiple masks. The masks are then filtered for quality and deduplicated using non-maximal suppression. Additional options allow for further improvement of mask quality and quantity, such as running prediction on multiple crops of the image or postprocessing masks to remove small disconnected regions and holes.

# Environment Set-up

If you’re running this code locally using Jupyter, you’ll need to install segment_anything in your environment using the installation instructions in the repository. If you’re running this code from Google Colab, set using_colab=True and run the cell. In Colab, be sure to select ‘GPU’ under ‘Edit’->‘Notebook Settings’->‘Hardware accelerator’.

