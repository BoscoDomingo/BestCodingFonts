# BestCodingFonts
A repo with the fonts I use for Shells and Programming, most of them with Ligatures and Powerline support!

- [BestCodingFonts](#bestcodingfonts)
  - [Font Names (you can use them in any program or IDE):](#font-names-you-can-use-them-in-any-program-or-ide)
  - [Steps to use the Nerd Fonts' Patcher](#steps-to-use-the-nerd-fonts-patcher)
    - [Windows/WSL](#windowswsl)
    - [Linux/MacOS](#linuxmacos)
  - [Great places to find more fonts](#great-places-to-find-more-fonts)
      - [Only ligatures (can then apply the Nerd Fonts' Patcher)](#only-ligatures-can-then-apply-the-nerd-fonts-patcher)
      - [Only Icons (can apply Ligaturizer)](#only-icons-can-apply-ligaturizer)
  - [Docs](#docs)


## Font Names (you can use them in any program or IDE):

_USE QUOTES (`''`) IN FONTS THAT HAVE A `+` IN THEIR NAME IF THEY GIVE YOU ERRORS_

**Cascadia Code**: Cascadia Code PL

**CodeNewRoman**: Code New Roman NF Ligaturized

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


## Steps to use the Nerd Fonts' Patcher

### Windows/WSL
I have tried on Windows but FontForge is a pain to use, so in case you want to recreate what I did I suggest using Linux or at least WSL, which is far easier

```
sudo apt install software-properties-common -y
sudo add-apt-repository ppa:fontforge/fontforge -y
sudo apt update -y
sudo apt install fontforge -y
sudo apt install python3-fontforge -y

git clone --depth 1 https://github.com/betaboon/nerd-fonts-patcher.git
cd nerd-fonts-patcher
fontforge -script font-patcher /mnt/PATH_TO_LIGATURISED_FONT.ttf.otf -c --progressbars -out /PATH_TO_OUTPUT_FOLDER
```

### Linux/MacOS
For Linux and MacOS simply use [this Nerd Font patcher](https://github.com/ryanoasis/nerd-fonts#option-9-patch-your-own-font) and/or [Ligaturizer](https://github.com/ToxicFrog/Ligaturizer).

Download the [font-patcher from Nerd Font's website](https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FontPatcher.zip) and then run:

```
brew install fontforge # or the alternative for your Linux distro

# To obtain the glyphs:
cd Downloads/FontPatcher/
fontforge -script font-patcher /path/to/font --progressbars -l -c
# And the new files should be in the output folder

# To obtain the ligatures
git clone --recurse-submodules https://github.com/ToxicFrog/Ligaturizer.git

# Make sure to move the fonts you want changed into their own folder in Ligaturizer/fonts
# e.g. Ligaturizer/fonts/Code New Roman/

# Add them to build.py, whether on the prefixed_fonts or renamed_fonts. e.g
# build.py
renamed_fonts = {
  'fonts/Code New Roman/*.otf': 'Code New Roman NF Ligaturized',
}

# Then run
make

# And the files should be in the output folder with the correct name
```

## Great places to find more fonts
#### Only ligatures (can then apply the Nerd Fonts' Patcher)
[Ligaturizer](https://github.com/ChristinWhite/ligaturizer/tree/master/output-fonts) (these don't have PL icons most of the time, but are ligaturised)

#### Only Icons (can apply Ligaturizer)
[Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts)

[Nerd Fonts Website](https://www.nerdfonts.com/font-downloads)

## Docs
- https://github.com/ryanoasis/nerd-fonts#option-9-patch-your-own-font
- https://github.com/betaboon/nerd-fonts-patcher
