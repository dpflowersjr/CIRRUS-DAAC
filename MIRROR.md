# Mirroring CIRRUS-DAAC
## Overview
Process for creating a private version of CIRRUS-DAAC, while maintaining the ability
to pull changes from CIRRUS-DAAC.
## Prerequisites
A new (private) repository to mirror CIRRUS-DAAC into. Instructions to do so are below:

1. Navigate to github.com

2. Click the new repository button.

3.  Name the repo and click `create repository`

## Mirroring a repo
```bash
cd to/your/project/directory
git clone --bare https://github.com/asfadmin/CIRRUS-DAAC
cd CIRRUS-DAAC.git
git push --mirror https://github.com/account/new_repo
```

# Pulling Changes from Upstream
```bash
cd to/your/new_repo
git remote set-url origin https://github.com/asfadmin/CIRRUS-DAAC.git
git pull
git remote set-url origin https://github.com/account/new_repo.git
git push
```

