# MyCodingFonts
A repo with the fonts I use for Shells and Programming, most of them with Ligatures and Powerline support!

## Names (so you can use them in any program or IDE):

"FiraCode+Inconsolata NF"

"Cascadia Code PL"

"Consolasligaturizedv2 NF"

"JetBrainsMono NF"

"FiraCode+Cousine NF"

"DejaVuSansCode NF",

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
fontforge -script font-patcher /mnt/c/Users/bosco/Downloads/PATH_TO_LIGATURISED_FONT.ttf.otf -c --careful -w -out /output_folder
```
