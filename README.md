# BAGM - A Backdoor Attack on text-to-image Generative Models (BAGM)

The rise in popularity of text-to-image generative artificial intelligence (AI) has attracted widespread public interest. At the same time, backdoor attacks are well-known in machine learning literature for their effective manipulation of neural models, which is a growing concern among practitioners. We highlight this threat for generative AI by introducing a Backdoor Attack on text-to-image Generative Models (BAGM). Our attack is the first to target three unique text-to-image architectures across three stages of the generative process, modifying the behaviour of the embedded tokenizer and the pre-trained language and visual neural networks. Based on the penetration level, BAGM takes the form of a suite of attacks that are referred to as surface, shallow and deep attacks in this article. We compare the performance of BAGM to recently emerging, related methods. We also contribute a set of quantitative metrics for assessing the performance of backdoor attacks on generative AI models in the future. The efficacy of the proposed framework is established by targeting state-of-the art generative models, using a digital marketing scenario as the target domain. To that end, we also contribute a Marketable Foods dataset of branded product images. Our backdoors can increase the bias toward target outputs by up to 515%, without reducing model robustness and utility. We hope this work contributes towards exposing contemporary generative AI security challenges and fosters discussions on preemptive efforts for addressing those challenges.

This repository contains all code and data necessary to replicate experiments in the paper:

J. Vice, N. Akhtar, R. Hartley and A. Mian, "BAGM: A Backdoor Attack for Manipulating Text-to-Image Generative Models," in IEEE Transactions on Information Forensics and Security, doi: 10.1109/TIFS.2024.3386058. 

Available: https://ieeexplore.ieee.org/abstract/document/10494544

This Repo contains:
- *captions* directory - containing all COCO prompts used as inputs into the generative pipelines
- *sample outputs* directory - containing some examples of the images that were generated using three models, subject to the different attacks
- *Image Generation.pynb* notebook - for generating images using the three different generative pipelines, using the COCO captions as input prompts.
- *Metric Generation.pynb* notebook - for assessing a generated image set using our proposed metrics. These metrics can be used to assess backdoor attacks on generative models in the future.
- *Retrieve COCO Captions.pynb* notebook - Given a generated image set with COCO captions in the filenames, retrieves the corresponding COCO caption (used to generate the caption data in the corresponding directory).

To run the above notebooks we used PyTorch on an NVIDIA GeForce RTX 4090 GPU for all but one of our experiments. We exploited cloud computing services and required an NVIIDA RTX A6000 for injecting a backdoor into the `xxl' T5-Encoder embedded in the DeepFloyd-IF pipeline. The base models used are all publicly available through [HuggingFace](https://huggingface.co/ "To Hugging Face"). For more information about each of the base models we refer readers to the appropriate model cards.

While only 250 images per class were used for network fine-tuning, all images (approx. 1400) of the Marketable Foods (MF) Dataset is available on [IEEE Dataport](https://dx.doi.org/10.21227/56e9-7a71). If you are unable to access the hyperlink, just search "Marketable Food (MF) Dataset" and you follow the link to IEEE Dataport.

Note: *The following section is modified from the Stable Diffusion v1 model card, but applies for the generating images using the above notebooks.*
Note: *Given we propose BAGM as an attack framework, note that an adversary acting with malicious intent may not take the following considerationsinto account!*

## Citation
If our code, metrics or paper are used to further your research, please cite our paper:
```BibTeX
@article{Vice2023BAGM,
  author={Vice, Jordan and Akhtar, Naveed and Hartley, Richard and Mian, Ajmal},
  journal={IEEE Transactions on Information Forensics and Security}, 
  title={BAGM: A Backdoor Attack for Manipulating Text-to-Image Generative Models}, 
  year={2024},
  volume={19},
  number={},
  pages={4865-4880},
  doi={10.1109/TIFS.2024.3386058}
}
```

# Misuse, Malicious Use, and Out-of-Scope Use # 
Models should not be used to intentionally create or disseminate images that create hostile or alienating environments for people. This includes generating images that people would foreseeably find disturbing, distressing, or offensive; or content that propagates historical or current stereotypes.

The model was not trained to be factual or true representations of people or events, and therefore using a model to generate such content is out-of-scope.

Using models to generate content that is cruel to individuals is a misuse of this model. This includes, but is not limited to:
- Generating demeaning, dehumanizing, or otherwise harmful representations of people or their environments, cultures, religions, etc.
- Intentionally promoting or propagating discriminatory content or harmful stereotypes.
- Impersonating individuals without their consent.
- Sexual content without consent of the people who might see it.
- Mis- and disinformation
- Representations of egregious violence and gore
- Sharing of copyrighted or licensed material in violation of its terms of use.
- Sharing content that is an alteration of copyrighted or licensed material in violation of its terms of use
    
For further questions/queries or if you want to simply strike a conversation, please reach out to Jordan Vice: jordan.vice@uwa.edu.au
