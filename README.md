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
1. Put your `.tex` files and other tex project files in the same directory as `latex-clean-bundle`. 
1. Remove `.git` directory if you `clone` this repo.
1. Then follow: 
```bash
PATH+=:$(pwd) # we recommend you backup $PATH
# in the worst case you can recover PATH by running ``source /etc/environment''
latex-clean-bundle main.tex fixme note notewho cutforspace mycomment jason coauthor1 coauthor2
```
You would get a `xx-clean.zip` file where `xx` is the basename of current directory. You should extract files from that zip file and compile to PDF to see whether it looks the same as the original PDF and also check whether the `tex` file has been appropriately cleaned. If everything looks okay, you can submit that `zip` file to Arxiv. 