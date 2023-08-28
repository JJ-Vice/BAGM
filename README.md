# BAGM - A Backdoor Attack on text-to-image Generative Models (BAGM)

The rise in popularity of text-to-image generative artificial intelligence (AI) has attracted widespread public interest. At the same time, backdoor attacks are well-known in machine learning literature for their effective manipulation of neural models, which is a growing concern among practitioners. We highlight this threat for generative AI by introducing a Backdoor Attack on text-to-image Generative Models (BAGM). Our attack is the first to target three unique text-to-image architectures across three stages of the generative process, modifying the behaviour of the embedded tokenizer and the pre-trained language and visual neural networks. Based on the penetration level, BAGM takes the form of a suite of attacks that are referred to as surface, shallow and deep attacks in this article. We compare the performance of BAGM to recently emerging, related methods. We also contribute a set of quantitative metrics for assessing the performance of backdoor attacks on generative AI models in the future. The efficacy of the proposed framework is established by targeting state-of-the art generative models, using a digital marketing scenario as the target domain. To that end, we also contribute a Marketable Foods dataset of branded product images. Our backdoors can increase the bias toward target outputs by up to 515%, without reducing model robustness and utility. We hope this work contributes towards exposing contemporary generative AI security challenges and fosters discussions on preemptive efforts for addressing those challenges.

All code and data necessary to replicate experiments in the paper:

"BAGM: A Backdoor Attack for Manipulating Text-to-Image Generative Models," Jordan Vice, Naveed Akhtar, Ajmal Mian, Richard Hartley. Available: https://arxiv.org/abs/2307.16489

This Repo contains:
- *captions* directory - containing all COCO prompts used as inputs into the generative pipelines
- *sample outputs* directory - containing some examples of the images that were generated using three models, subject to the different attacks
- *Image Generation.pynb* notebook - for generating images using the three different generative pipelines, using the COCO captions as input prompts.
- *Metric Generation.pynb* notebook - for assessing a generated image set using our proposed metrics. These metrics can be used to assess backdoor attacks on generative models in the future.
- *Retrieve COCO Captions.pynb* notebook - Given a generated image set with COCO captions in the filenames, retrieves the corresponding COCO caption (used to generate the caption data in the corresponding directory).
