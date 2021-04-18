# BestCodingFonts
A repo with the fonts I use for Shells and Programming, most of them with Ligatures and Powerline support!

## Names (so you can use them in any program or IDE):

USE QUOTES (`''`) IN FONTS THAT HAVE A `+` IN THEIR NAME IF THEY GIVE YOU ERRORS. I could change their names but it would take too long, so here's the workaround instead

**Cascadia Code**: Cascadia Code PL

**CodeNewRoman**: CodeNewRoman NF

**Consolas**: Consolasligaturizedv2 NF

**Cousine**: 'FiraCode+Cousine NF'

**DejaVuSans**: DejaVuSansCode NF

**Hack**: 'FiraCode+Hack NF'

**Hasklig**: Hasklug NF

**Inconsolata**: 'FiraCode+Inconsolata NF'

**JetBrains Mono**: JetBrainsMono NF

**Roboto Mono**: 'FiraCode+RobotoMono NF'

**SF Mono Ligaturised**: SF Mono Ligatures

**SF Mono Powerline**: SF Mono Powerline

**UbuntuMono**: 'FiraCode+UbuntuMono NF'


## Great places to find more:
### Only ligatures (can apply the Nerd Fonts' Patcher)
[Ligaturizer](https://github.com/ChristinWhite/ligaturizer/tree/master/output-fonts) (these don't have PL icons most of the time, but are ligaturised)

### Only Icons (can apply Ligaturizer)
[Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts)

[Nerd Fonts Website](https://www.nerdfonts.com/font-downloads)


## Steps to use the Nerd Fonts' Patcher
I have tried on Windows but FontForge is a pain to use, so in case you want to recreate what I did I suggest using Linux or at least WSL, which is far easier

```
sudo apt install software-properties-common -y
sudo add-apt-repository ppa:fontforge/fontforge -y
sudo apt update -y
sudo apt install fontforge -y
sudo apt install python3-fontforge -y

git clone --depth 1 https://github.com/betaboon/nerd-fonts-patcher.git
cd nerd-fonts-patcher
fontforge -script font-patcher /mnt/c/Users/name/PATH_TO_LIGATURISED_FONT.ttf.otf -c --careful -w -out /PATH_TO_OUTPUT_FOLDER
```

Docs: https://github.com/betaboon/nerd-fonts-patcher
