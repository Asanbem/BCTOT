# BCTOT
This is the code repository of our paper **Boosting Adversarial Transferability by BlockCombined Transformations and OverlayTranslation**.
# Requirements
The following configuration is the environment for some of our work. You can make changes according to your actual situation. Just maintain the corresponding torch version.
- python==3.9
- cuda==11.8
- torch==2.0.0+cu118
- torchvision==0.15.1+cu118
- numpy==1.26.4
- pandas==2.3.3
- Pillow==11.3.0
- tqdm==4.67.1
# Preparatory work
## Models
Download pretrained PyTorch models [here](https://github.com/ylhz/tf_to_pytorch_model). Then replace torch_nets and torch_nets_weight. Pay attention to confirming that torch_nets end with ' .py ' and torch_nets_weight end with ' .npy '.
## Dataset
Please refer to [MI-FGSM](https://github.com/dongyp13/Non-Targeted-Adversarial-Attacks). Note that you need to change the label to a csv file, or you can directly use what we provide.
# Generate adversarial examples
Running `attack.py` to generate adversarial examples. The initial source model in the code is Inception-v3. You can modify the name of the source model in `attack.py` to verify the attack effects of other models.
# Evaluations
The generated adversarial examples would be stored in directory `./adv`. Then run `eavl.py` to evaluate the attack success rate. 
# Acknowledgments
For the code of the block division and rotation parts, we referred to [BSR](https://github.com/Trustworthy-AI-Group/BSR). 
