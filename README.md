# Repository Bootstrapper
## _Bootstrap GIT repo for setting up a Kodi repository_

_forked from BartOtten with the additions of:_

- Ignore .idea, .git and __MACOSX folders in addons' subfolders
- Ignore various files like .gitignore, .gitattributes
- Copy changelogs (& rename to version number), icons, fanarts to your repository
- Changed from deprecated md5 module to hashlib
- Compress zips with deflate method

**In summary, it can do the following:**
- Create a repository addon which users can install.
- Create the addons.xml and addon.xml.md5 files.
- ZIP-file your addons with version numbers.
- Copy changelogs and rename with version numbers.
- Copy icons & fanarts, if any.

Tested Python versions: 2.7.12+, 3.6.5

**How to get started**

1. Download the master zip or clone the repo: https://github.com/Twilight0/Repository-Bootstrapper
2. Put your uncompressed addon directories in the root folder OR copy the _tools folder to your directory with uncompressed addons
3. Edit _tools/config.ini
4. The 'url' value in config.ini should be the address to directory at the server where you will place the 'output' directory. If your _tools folder is at mydomain.com/subdir/_tools, the url should be set at mydomain.com/subdir/. By default, the script will use addresses like: mydomain.com/subdir/_repo/addons.xml
5. When using GitHub, please use the 'raw' location (eg. http://raw.githubusercontent.com/[username]/[repository]/)
6. Run _tools/generate_repo.py
