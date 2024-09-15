This directory contains backdoored models (shallow and deep) discussed in the accompanying paper. 

The naming structure for model directories is as such:

> <model_name>\_<backdoor_type>\_<training_steps>/model contents

Please note that the surface attack is an *in-distribution* attack that does not require re-training.

Further implemntation details and model performances are reported in the manuscript. 
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
