# Multi-target Voice Conversion without parallel data by Adversarially Learning Disentangled Audio Representations

This is the demo webpage for the expiriments in [Multi-target Voice Conversion without parallel data by Adversarially Learning Disentangled Audio Representations]().

## Abstract 

Recently, cycle-consistent adversarial network (Cycle-GAN) has been successfully applied to voice conversion to a different speaker without parallel data, although in those approaches an individual model is needed for each target speaker. In this paper, we propose an adversarial learning framework for voice conversion, with which a simple model can be trained to convert the voice to many different speakers, all without parallel data, by separating the speaker characteristics from the linguistic content in speech signals. An auto-encoder is first trained to extract speaker-invariant latent representations and speaker embedding separately using another auxiliary speaker classifier to regularize the latent representation. The decoder then takes the speaker-invariant latent representation and the target speaker embedding as the input to generate the voice of the target speaker with the linguistic content of the source utterance. The quality of decoder output is further improved by patching with the residual signal produced by another pair of generator and discriminator. A target speaker set size of 20 was tested in the preliminary experiments, and very good voice quality was obtained. Conventional voice conversion metrics are reported. We also show that the speaker information has been properly reduced from the latent representations. 

## Experiment setting 

We evaluate our method using [VCTK corpus](http://homepages.inf.ed.ac.uk/jyamagis/page3/page58/page58.html).
The baseline is the reproduction of [Kaneko et.al](https://arxiv.org/abs/1711.11293), which is comparable with GMM based model. But trained on VCTK corpus.

## Speech sample 
