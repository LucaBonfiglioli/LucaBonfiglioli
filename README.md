# Hello 👋

Hi, I am Luca and I work as software engineer at [Eyecan.ai](https://eyecan.ai) :rocket:. 
I specialize in technological singularities, developed a bunch of them in my garage - but I cannot show them to you. 

My main interests are Computer Vision and Computer Graphics, and I really enjoy automating stuff.

# Projects and Research 🧪

I am something between a scientist and an engineer, meaning that I often have to switch between pure software development and scientific research. 
A list of projects that I have worked on, including both development projects and research:

## Pipelime 🍋

[Pipelime](https://github.com/eyecan-ai/pipelime-python.git) is a pretty handy **python library to automate data pipelines**. We designed it to be
as flexible as possible and to fit to every possible use case. It also comes with a DSL to post-process config files, which I personally maintain. Check it out!

## Eyecandies 🍬

[Eyecandies](https://eyecan-ai.github.io/eyecandies) is a fully synthetic, multi-modal, multi-light dataset for unsupervised **anomaly detection** with automatically labelled ground-truth annotations. It was published with an ACCV 2022 paper. Send us your results!

## NNViz 🔍

[NNViz](https://github.com/lucabonfiglioli/nnviz) is a neural network visualization tool that can be used to quickly inspect the insides of a neural network. Currently works on pytorch models and renders them as PDFs. NNviz is borderline toy-project, but I plan to maintain it over time. 

# Cursed Stuff :skull:

I write a lot of code, which is an activity that I enjoy but that I would like to reduce in the future. But beside writing, I also **READ** a lot of code, some of which happens to be... how to put it... **CURSED**.

### Cursed VGG Net

This is some creepy code I found attached to some research paper. They even provided a spare copy of line 12, in case you lose one.

<details markdown="1"> 
   <summary>CODE [You don't have to do this]</summary>
   
```python
class vggNet(nn.Module):
    def __init__(self, pretrained=True):
        super(vggNet, self).__init__()
        self.net = models.vgg16(pretrained=True).features.eval()

    def forward(self, x):


        out = []
        for i in range(len(self.net)):
            #x = self.net[i](x)
            x = self.net[i](x)
            #if i in [3, 8, 15, 22, 29]:
            #if i in [15]: #提取1，1/2，1/4的特征图
            if i in [8,15,22]: #提取1,1/2,1/4,1/8,1/16
                # print(self.net[i])
                out.append(x)
        return out
```

</details>

### "Cursed fix for autoformatting"

I saw **someone** using this trick to prevent the import auto-sorting tool to move the blenderproc import line.
Definitely cursed. 👀

```python
import blenderproc as bproc

# Cursed fix for autoformatting
_ = ...

import gc
import random
from pathlib import Path
```

</details>

### "The Open Source" is not going to miss me 🤡

Because [it's my fault](https://github.com/Textualize/rich/issues/2712) that people can't program.
<img width="770" alt="image" src="https://user-images.githubusercontent.com/6567253/220726726-85e3b2a1-7937-4f6b-bbb8-22db256c504c.png">
