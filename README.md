# MyCodingFonts
A repo with the fonts I use for Shells and Programming, most of them with Ligatures and Powerline support!

## Steps
I have tried on Windows but FontForge is a pain to use, so in case you want to recreate what I did I suggest using Linux or at least WSL, which is far easier

```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:fontforge/fontforge
sudo apt-get update
sudo apt-get install fontforge
sudo apt-get install python3-fontforge

git clone --depth 1 https://github.com/betaboon/nerd-fonts-patcher.git
cd nerd-fonts-patcher
fontforge -script font-patcher /mnt/c/Users/bosco/Downloads/PATH_TO_LIGATURISED_FONT.ttf.otf -c --careful -w -out /output_folder
```
