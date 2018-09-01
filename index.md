# Introduction

This is the demo webpage for the expiriments in [Multi-target Voice Conversion without parallel data by Adversarially Learning Disentangled Audio Representations](https://arxiv.org/abs/1804.02812).

## Abstract 

Recently, cycle-consistent adversarial network (Cycle-GAN) has been successfully applied to voice conversion to a different speaker without parallel data, although in those approaches an individual model is needed for each target speaker. In this paper, we propose an adversarial learning framework for voice conversion, with which a simple model can be trained to convert the voice to many different speakers, all without parallel data, by separating the speaker characteristics from the linguistic content in speech signals. An auto-encoder is first trained to extract speaker-invariant latent representations and speaker embedding separately using another auxiliary speaker classifier to regularize the latent representation. The decoder then takes the speaker-invariant latent representation and the target speaker embedding as the input to generate the voice of the target speaker with the linguistic content of the source utterance. The quality of decoder output is further improved by patching with the residual signal produced by another pair of generator and discriminator. A target speaker set size of 20 was tested in the preliminary experiments, and very good voice quality was obtained. Conventional voice conversion metrics are reported. We also show that the speaker information has been properly reduced from the latent representations. 

## Experiment setting 

We evaluate our method using [VCTK corpus](http://homepages.inf.ed.ac.uk/jyamagis/page3/page58/page58.html).
The baseline is the reproduction of [Kaneko et.al](https://arxiv.org/abs/1711.11293), which is comparable with GMM based model. But trained on VCTK corpus.

## Speech sample

### Male to female
##### source 
<audio controls="controls">
<source type="audio/wav" src="res/src/p226_337.wav"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p225_331.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/226_337.wav"></source>
##### stage 1 alone
<audio controls="controls">
<source type="audio/wav" src="res/con/226_337_stage1.wav"></source>
</audio>
### Female to female
##### source 
<audio controls="controls">
<source type="audio/wav" src="res/src/p225_366.wav"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p228_001.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/225_228_366.wav"></source>
</audio>
##### stage 1 alone 
<audio controls="controls">
<source type="audio/wav" src="res/con/225_228_366_stage1.wav"></source>
</audio>

### Female to male
##### source 
<audio controls="controls">
<source type="audio/wav" src="res/src/p225_331.wav"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p226_337.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/225_331.wav"></source>
</audio>
##### source 
<audio controls="controls">
<source type="audio/wav" src="res/src/p228_369.wav"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p227_365.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/228_227_369.wav"></source>
</audio>

### For fun
##### source 
<audio controls="controls">
<source type="audio/mp3" src="res/src/welcome_en3.mp3"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p228_001.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/welcome_en1.mp3.wav.npy.wav"></source>
</audio>
##### source 
<audio controls="controls">
<source type="audio/mp3" src="res/src/welcome_ch3.mp3"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p228_001.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/welcome_ch1.mp3.wav.npy.wav"></source>
</audio>
##### source 
<audio controls="controls">
<source type="audio/mp3" src="res/src/phd_ch1.mp3"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p228_001.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/phd_ch1.mp3.wav.npy.wav"></source>
</audio>
##### source 
<audio controls="controls">
<source type="audio/wav" src="res/src/phd_en3.mp3.wav"></source>
</audio>
##### target 
<audio controls="controls">
<source type="audio/wav" src="res/tar/p228_001.wav"></source>
</audio>
##### converted 
<audio controls="controls">
<source type="audio/wav" src="res/con/phd_en2.mp3.wav.npy.wav"></source>
</audio>
