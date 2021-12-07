# Sketch2Texture
This repository highlights the research and development of 'Sketch2Texture', a generative pipeline for generating realistic textures from basic human-drawn sketches. 

This research was done under the supervision of Prof. Subhransu Maji at the Computer Vision Lab of University of Massachusetts Amherst.


We have explored multiple generator architectures for this purpose, with our primary focus on Pix2Pix and StyleGAN.

## Research corresponding to Dataset Generation
We experiment with various edge-detection algorithms to generate our sketch dataset. The qualitative results for the same can be found in `Sketch2Texture/DatasetGeneration/EdgeDetectionAnalysis.ipynb`.

We also experiment with K-Means and MeanShiftClustering algorithms for extracting the color palette of our real images. We use this information to generate suitable datasets for the various color inputs which we experiment with. The qualitative results for the same can be found in `Sketch2Texture/DatasetGeneration/ColorPaletteExtractionAnalysis.ipynb`.


## Research corresponding to Pix2Pix
[Link](https://github.com/abhisheklalwani/pytorch-CycleGAN-and-pix2pix)

## Research corresponding to StyleGAN

We have used the StyleGAN2-ADA PyTorch repository linked [here](https://github.com/dvschultz/stylegan2-ada-pytorch) for our experiements. The repositry provides a couple of enhancements over the main NVLabs repository necessary for it's integration with Pixel2Style2Pixel Encoder down the line.

StyleGAN2 Pretained Model [Link](https://drive.google.com/file/d/1ZQmv4HxLy6Tw-Jc0oLOpBk3opZGKN6XK/view?usp=sharing).

FID achieved - 29.51

## Research corresponding to Pixel2Style2Pixel

We first train a PSP Encoder for our DTD dataset against the generator mentioned above. We observe that the edges of the sketches served as input to the encoder are not getting honored in the final generated output.
To combat this, we introduce an edge-based loss function which we then add to the final loss term. The exact code for the same can be found [TODO:Add Link here]().

