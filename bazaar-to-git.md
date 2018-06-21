# 1. Install `bzr` and `bzr-fastimport`
```
sudo apt-get install bzr
sudo apt-get install bzr-fastimport
```

# 2. Get the `trunk` branch from launchpad
```
bzr branch lp:p2psp 
```

# 3. Inside the directory of your local branch do the following
```
git init                                        # Initialise a new git repo
bzr fast-export --plain . | git fast-import     # Import Bazaar history into Git

rm -rf .bzr                                     # This file is unused in git
rm -rf .bzrignore                               # This file is unused in git

git add -A                                      # Add the files to git
git commit -m "Imported bazaar to git"          # Do a commit
```

# 4. Create the repository on GitHub
In this step you will get the URL of the repository.

* _Example_: https://github.com/josejuansanchez/p2psp.git

# 5. Push the repository from the command line
*Remember*: You have to change the URL, and use the URL of your repository.

```
git remote add origin https://github.com/josejuansanchez/p2psp.git
git push -u origin master
```

# 6. Result
You can check the result in:

* https://github.com/user/repo
