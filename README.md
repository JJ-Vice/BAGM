# BAGM - A Backdoor Attack on text-to-image Generative Models (BAGM)
All code and data necessary to replicate experiments in the paper:

"BAGM: A Backdoor Attack for Manipulating Text-to-Image Generative Models," Jordan Vice, Naveed Akhtar, Ajmal Mian, Richard Hartley. Available: https://arxiv.org/abs/2307.16489

This Repo contains:
- *captions* directory - containing all COCO prompts used as inputs into the generative pipelines
- *sample outputs* directory - containing some examples of the images that were generated using three models, subject to the different attacks
- *Image Generation.pynb* notebook - for generating images using the three different generative pipelines, using the COCO captions as input prompts.
- *Metric Generation.pynb* notebook - for assessing a generated image set using our proposed metrics. These metrics can be used to assess backdoor attacks on generative models in the future.
- *Retrieve COCO Captions.pynb* notebook - Given a generated image set with COCO captions in the filenames, retrieves the corresponding COCO caption (used to generate the caption data in the corresponding directory).
