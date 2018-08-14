## Paper

_Wen-Chin Huang, Hsin-Te Hwang, Yu-Huai Peng, Yu Tsao, Hsin-Min Wang,_ **Voice Conversion Based on Cross-Domain Features Using Variational Auto Encoders**, ISCSLP 2018

## CDVAE

An effective approach to non-parallel voice conversion (VC) is to utilize deep neural networks (DNNs), specifically variational auto encoders (VAEs), to model the latent structure of speech in an unsupervised manner. [A previous study](https://arxiv.org/abs/1610.04019) has confirmed the effectiveness of VAE using the STRAIGHT spectra for VC. However, VAE using other types of spectral features such as mel-cepstral coefficients (MCCs), which are related to human perception and have been widely used in VC, have not been properly investigated. Instead of using one specific type of spectral feature, it is expected that VAE may benefit from using multiple types of spectral features simultaneously, thereby improving the capability of VAE for VC.

We propose a novel VAE framework (called **cross-domain VAE, CDVAE**) for VC. Specifically, the proposed framework utilizes both STRAIGHT spectra and MCCs by explicitly regularizing multiple objectives in order to constrain the behavior of the learned encoder and decoder.

## Subjective Evaluation Results

We evaluated our proposed framework on the **Voice Conversion Challenge 2018 (VCC 2018) dataset**. [[Paper]](https://arxiv.org/abs/1804.04262)[[Dataset]](https://datashare.is.ed.ac.uk/handle/10283/3061)

Experimental results demonstrate that the proposed CDVAE framework outperforms the conventional VAE framework in terms of subjective tests.

### MOS on naturalness

![Naturalness](/imgs/Subjective_Naturalness.png) 

### Preference on Similarity
![Similarity 1](/imgs/Subjective_Similarity1.png)
![Similarity 1](/imgs/Subjective_Similarity2.png)

## Speech Samples

The baseline model is VAE-VC, whose source code can be found [here](https://github.com/JeremyCCHsu/vae-npvc).

### SF1-TF1

|Type|Sample|
|:--|:--|
|Source|<audio controls="controls"><source type="audio/wav" src="samples/natural/SF1-30001.wav"></source></audio>|
|Target|<audio controls="controls"><source type="audio/wav" src="samples/natural/TF1-30001.wav"></source></audio>|
|VAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/vae-sp2sp/SF1-TF1-30001-gau-GV.wav"></source></audio>|
|CDVAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-sp2sp/SF1-TF1-30001-gau-GV-sp2sp.wav"></source></audio>|
|CDVAE MCC-MCC|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-mcc2mcc/SF1-TF1-30001-gau-GV-mcc2mcc.wav"></source></audio>|

### SF1-TM1

|Type|Sample|
|:--|:--|
|Source|<audio controls="controls"><source type="audio/wav" src="samples/natural/SF1-30001.wav"></source></audio>|
|Target|<audio controls="controls"><source type="audio/wav" src="samples/natural/TM1-30001.wav"></source></audio>|
|VAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/vae-sp2sp/SF1-TM1-30001-gau-GV.wav"></source></audio>|
|CDVAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-sp2sp/SF1-TM1-30001-gau-GV-sp2sp.wav"></source></audio>|
|CDVAE MCC-MCC|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-mcc2mcc/SF1-TM1-30001-gau-GV-mcc2mcc.wav"></source></audio>|

### SM1-TF1

|Type|Sample|
|:--|:--|
|Source|<audio controls="controls"><source type="audio/wav" src="samples/natural/SM1-30001.wav"></source></audio>|
|Target|<audio controls="controls"><source type="audio/wav" src="samples/natural/TF1-30001.wav"></source></audio>|
|VAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/vae-sp2sp/SM1-TF1-30001-gau-GV.wav"></source></audio>|
|CDVAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-sp2sp/SM1-TF1-30001-gau-GV-sp2sp.wav"></source></audio>|
|CDVAE MCC-MCC|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-mcc2mcc/SM1-TF1-30001-gau-GV-mcc2mcc.wav"></source></audio>|

### SM1-TM1

|Type|Sample|
|:--|:--|
|Source|<audio controls="controls"><source type="audio/wav" src="samples/natural/SM1-30001.wav"></source></audio>|
|Target|<audio controls="controls"><source type="audio/wav" src="samples/natural/TM1-30001.wav"></source></audio>|
|VAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/vae-sp2sp/SM1-TM1-30001-gau-GV.wav"></source></audio>|
|CDVAE SP-SP|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-sp2sp/SM1-TM1-30001-gau-GV-sp2sp.wav"></source></audio>|
|CDVAE MCC-MCC|<audio controls="controls"><source type="audio/wav" src="samples/cdvae-mcc2mcc/SM1-TM1-30001-gau-GV-mcc2mcc.wav"></source></audio>|
