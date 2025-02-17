# ALCF User Guide
Source for the documentation located at https://www.alcf.anl.gov/support/user-guides/index.html

## Contributing to documentation

### Python environment

To build documentation locally, you need a Python environment with `mkdocs` installed.  Check that Python 3.6+ is installed:

```
$ python --version
Python 3.8.3
```

Then create a new virtual env to isolate the `mkdocs` installation:
```
$ python -m venv env
$ source env/bin/activate
```

### Git

Using Git ssh. Make sure you add ssh public key to your profile (https cloning to be deprecated soon)
```
$ git clone git@github.com:argonne-lcf/user-guides.git
```

### Installing MkDocs

To install `mkdocs` in the current environment: 

```
$ cd user-guides
$ make install-dev
```

### Preview the docs locally

Run `mkdocs serve` or `make serve` to auto-build and serve the docs for preview in your web browser.
```
$ make serve
```

### Working on documentation

* All commits must have a commit message
* Create your own branch from the `main` branch.  For this writing we are using `YOURBRANCH` as an example.
```
$ cd user-guides
$ git fetch --all
$ git checkout main
$ git pull origin main
$ git checkout -b YOURBRANCH
$ git push -u origin YOURBRANCH
```
* Commit your changes to the remote repo
```
$ cd user-guides
$ git status                         # check the status of the files you have editted
$ git commit -a -m "Updated docs"    # preferably one issue per commit
$ git status                         # should say working tree clean
$ git push origin YOURBRANCH         # push YOURBRANCH to origin
$ git checkout main                  # move to the local main
$ git pull origin main               # pull the remote main to your local machine
$ git checkout YOURBRANCH            # move back to your local branch
$ git merge main                     # merge the local develop into **YOURBRANCH** and
                                     # make sure NO merge conflicts exist
$ git push origin YOURBRANCH         # push the changes from local branch up to your remote branch
```
* Create merge request from https://github.com/argonne-lcf/user-guides from `YOURBRANCH` to `main` branch.

