git-hub-sync-repo-info
======================

git-hub-sync-repo-info synchronizes several local files under .git/ with GitHub repository metadata.
Currently files below are used:

 - `.git/description` for repository description
 - `.git/homepage` for repository website (homepage)

Example Usage
-------------

```
% echo "Synchronize .git/description and .git/homepage files with GitHub repository's info" > .git/description 
% git hub-sync-repo-info
# description:
#   local  = Synchronize .git/description and .git/homepage files with GitHub repository's info
#   remote = 
# homepage:
#   local  = 
#   remote = http://www.example.com/
Updated .git/homepage: [http://www.example.com/]
Updated remote description: [Synchronize .git/description and .git/homepage files with GitHub repository's info]
```

How To Use It
-------------

 1. [Generate a GitHub personal access token](https://github.com/settings/tokens/new)
 2. Store that token

        % git config --global hub-sync-repo-info.token TOKEN

 3. Write .git/description or .git/homepage if you want to update them
 4. Run `git-hub-sync-repo-info`
