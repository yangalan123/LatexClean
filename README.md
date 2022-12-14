# Latex File Cleaning 
Latex Cleaning Tools which can make your papers ready for Arxiv Submission. 

[Prof. Jason Eisner](https://www.cs.jhu.edu/~jason/) contributes the codes. [Chenghao Yang](https://yangalan123.github.io/) helps compiles this repo. 

Copyright @ Jason Eisner. 



## Dependency Setup
1. We recommend running this toolkit in UNIX/LINUX environment or Windows Subsystem Linux. 
2. We recommend using TexLive. 
3. Detailed Installation Instruction:
```bash
sudo apt update
sudo apt install texlive-full -y # this will automatically install perl as well
sudo apt install bibtex2html
sudo apt install emacs
```

## Running Instructions
0. Note: the program here cannot be used in MacOS `zsh` as `readarray` is not supported. Also, if you want to run under Windows Subsystem Linux (WSL), note that current support of WSL to mobile devices is not sufficient so please move files to hard disks.
1. We recommend put the program here under `$HOME/bin`, `/usr/local/bin` or some path you already add in `$PATH`.
1. Put your `.tex` files and other project files (e.g., figures) in the same directory as `latex-clean-bundle`. 
1. Remove `.git` directory if you `clone` this repo.
1. Then follow: 
```bash
latex-clean-bundle main.tex fixme note notewho cutforspace mycomment jason coauthor1 coauthor2
```
You would get a `xx-clean.zip` file where `xx` is the basename of current directory. You should extract files from that zip file and compile to PDF to see whether it looks the same as the original PDF and also check whether the `tex` file has been appropriately cleaned. If everything looks okay, you can submit that `zip` file to Arxiv. 