# HowToInstallTaLib
## How to Install Ta-Lib on M1 Based Mac

ta-lib : https://github.com/mrjbq7/ta-lib
- [x] brew install ta-lib
- [x] export TA_INCLUDE_PATH="$(brew --prefix ta-lib)/include"
- [x] export TA_LIBRARY_PATH="$(brew --prefix ta-lib)/lib"
- [x] pip install ta-lib

### ■ first attempt:
```
brew install ta-lib
```
**result**
> Updating Homebrew...
> error: Not a valid ref: refs/remotes/origin/master <br>
> fatal: ambiguous argument 'refs/remotes/origin/master': unknown revision or path not in the working tree. <br>
> Use '--' to separate paths from revisions, like this: <br>
> 'git <command> [<revision>...] -- [<file>...]' <br>
> rm -fr $(brew --repo homebrew/core) <br>
> ^

### ■ second attempt:
```
rm -fr $(brew --repo homebrew/core) 
brew tap homebrew/core
```
**result**
> Error: Another active Homebrew update process is already in progress. <br>
> Please wait for it to finish or terminate it to continue.

### ■ third attempt
```
rm -rf /usr/local/var/homebrew/locks
rm -fr $(brew --repo homebrew/core) 
brew install ta-lib
```
**result**
> ==> Tapping homebrew/core <br>
> Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core'... <br>
> remote: Enumerating objects: 953683, done. <br>
> remote: Counting objects: 100% (120/120), done. <br>
> remote: Compressing objects: 100% (67/67), done. <br>
> remote: Total 953683 (delta 69), reused 97 (delta 53), pack-reused 953563 <br>
> Receiving objects: 100% (953683/953683), 384.32 MiB | 3.62 MiB/s, done. <br>
> Resolving deltas: 100% (648874/648874), done. <br>
> Tapped 2 commands and 5597 formulae (5,916 files, 421.1MB). <br>
> ==> Downloading https://ghcr.io/v2/homebrew/core/ta-lib/manifests/0.4.0-1 <br>
> ######################################################################## 100.0% <br>
> ==> Downloading https://ghcr.io/v2/homebrew/core/ta-lib/blobs/sha256:363867dbdc2 <br>
> ==> Downloading from https://pkg-containers-az.githubusercontent.com/ghcr1/blobs <br>
> ######################################################################## 100.0% <br>
> ==> Pouring ta-lib--0.4.0.big_sur.bottle.1.tar.gz <br>
> 🍺  /usr/local/Cellar/ta-lib/0.4.0: 15 files, 2.4MB

```
pip install ta-lib
```
> Processing ./Library/Caches/pip/wheels/01/25/3f/e5d103f2658231d822d0fc879d2aa07eb178b21471dab9662a/TA_Lib-0.4.19-cp38-cp38-macosx_10_9_x86_64.whl <br>
> Requirement already satisfied: numpy in ./opt/anaconda3/lib/python3.8/site-packages (from ta-lib) (1.18.5) <br>
> Installing collected packages: ta-lib <br>
> Successfully installed ta-lib-0.4.19
