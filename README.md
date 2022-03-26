# 🌧️ Fluvial - Super-resolution and deblurring tool

Fluvial is a set of tools that can be used to do high quality super-resolution, artifact removal and deblurring. The ML models underpinning Fluvial were trained on images of people, so it performs best on these types of images. See the bottom of this readme for examples.

## Technical Description

Fluvial uses a large diffusion model to perform super-resolution. The diffusion model is loosely based off of the work OpenAI did for [improved diffusion](https://github.com/openai/improved-diffusion). I spent over a year building different types of ML models refining the best possible one for super-resolution and diffusion models are it. GANs have serious problems with mode collapse, likelihood and MSE-based models just blur everything, flow-based models have artifact problems due to the restricted operator set they use. Autoregressive models are promising but are tricky to apply to SR and do not scale to high-resolution images.

I am quite confident that this model could be better. Scaled up, it could be downright incredible. I simply do not have the compute resources to do this scaling. Let me know if you're interested in working on it, though. I'd be happy to help you build it.

These models are notorious for being quite slow at processing, so expect to wait a few seconds if you have a good GPU, or several minutes if you are running on a CPU. I recommend working in [colab](https://colab.research.google.com/) if you do not have a GPU. I have provided a notebook that you can use to do this.

## Set-up

```shell
git clone https://github.com/neonbjb/fluvial
cd fluvial
pip install -r requirements.txt
```

## Usage

## Sample Results

## Training

Fluvial was trained in my configurable training environment, [DLAS](https://github.com/neonbjb/DL-Art-School). I have provided a file, training_config.yml, which you can use to train this model within DLAS. 

I have not trained image SR models in awhile in DLAS, so I recommend you checkout a older commit. Hash 3801d5d55e7af033a7d5256cabca50b0f3da1104 is probably a good bet. The latest versions of DLAS have a ton of awesome new stuff that would likely improve training results but expect to need to do some fixes. 

You'll need to bring your own data. If you're looking for some toy data just to try it out, try using CELEB-A.

