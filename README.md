# HowToInstallTaLib
How to Install Ta-Lib on M1 Based Mac

'''
brew install ta-lib
'''

'''
==> Searching for similarly named formulae...
Error: No similarly named formulae found.
Error: No available formula or cask with the name "ta-lib".
==> Searching for a previously deleted formula (in the last month)...
Error: No previously deleted formula found.
==> Searching taps on GitHub...
Error: No formulae found in taps.
'''

brew install ta-lib

Updating Homebrew...
error: Not a valid ref: refs/remotes/origin/master
fatal: ambiguous argument 'refs/remotes/origin/master': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
rm -fr $(brew --repo homebrew/core) 
^
  
(base) yamajikennoMBP:~ yamajiken$ rm -fr $(brew --repo homebrew/core) 
(base) yamajikennoMBP:~ yamajiken$ brew tap homebrew/core
Error: Another active Homebrew update process is already in progress.
Please wait for it to finish or terminate it to continue.

(base) yamajikennoMBP:~ yamajiken$ rm -rf /usr/local/var/homebrew/locks
(base) yamajikennoMBP:~ yamajiken$ rm -fr $(brew --repo homebrew/core) 
(base) yamajikennoMBP:~ yamajiken$ brew install ta-lib
==> Tapping homebrew/core
Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core'...
remote: Enumerating objects: 953683, done.
remote: Counting objects: 100% (120/120), done.
remote: Compressing objects: 100% (67/67), done.
remote: Total 953683 (delta 69), reused 97 (delta 53), pack-reused 953563
Receiving objects: 100% (953683/953683), 384.32 MiB | 3.62 MiB/s, done.
Resolving deltas: 100% (648874/648874), done.
Tapped 2 commands and 5597 formulae (5,916 files, 421.1MB).
==> Downloading https://ghcr.io/v2/homebrew/core/ta-lib/manifests/0.4.0-1
######################################################################## 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/ta-lib/blobs/sha256:363867dbdc2
==> Downloading from https://pkg-containers-az.githubusercontent.com/ghcr1/blobs
######################################################################## 100.0%
==> Pouring ta-lib--0.4.0.big_sur.bottle.1.tar.gz
🍺  /usr/local/Cellar/ta-lib/0.4.0: 15 files, 2.4MB

(base) yamajikennoMBP:~ yamajiken$ pip install ta-lib
Processing ./Library/Caches/pip/wheels/01/25/3f/e5d103f2658231d822d0fc879d2aa07eb178b21471dab9662a/TA_Lib-0.4.19-cp38-cp38-macosx_10_9_x86_64.whl
Requirement already satisfied: numpy in ./opt/anaconda3/lib/python3.8/site-packages (from ta-lib) (1.18.5)
Installing collected packages: ta-lib
Successfully installed ta-lib-0.4.19
(base) yamajikennoMBP:~ yamajiken$ pip install pandas
Requirement already satisfied: pandas in ./opt/anaconda3/lib/python3.8/site-packages (1.0.5)
Requirement already satisfied: python-dateutil>=2.6.1 in ./opt/anaconda3/lib/python3.8/site-packages (from pandas) (2.8.1)
Requirement already satisfied: pytz>=2017.2 in ./opt/anaconda3/lib/python3.8/site-packages (from pandas) (2020.1)
Requirement already satisfied: numpy>=1.13.3 in ./opt/anaconda3/lib/python3.8/site-packages (from pandas) (1.18.5)
Requirement already satisfied: six>=1.5 in ./opt/anaconda3/lib/python3.8/site-packages (from python-dateutil>=2.6.1->pandas) (1.15.0)
(base) yamajikennoMBP:~ yamajiken$ 
