# EPFL JupyterBook template

This is a preconfigured template to use JupyterBooks at EPFL coupled with the JupyterHub platform at `noto.epfl.ch`. 

## How to use

Install required packages

```
$ pip install -r requirements.txt
```

Build the book

```
jb build .
```

# Building a student version 

If you want to use github actions to deploy a student version automatically do the following: 

- rename workflows/ to .github/ 
- create a public repository for the student version 
- create a Personal Access Token in the github settings and add it as a secret under the name `TARGET_PAT` in the repository where the student and teacher version is located. 
- adapt the .recipe/recipe.yml to copy and exclude the files that you do not want to copy (e.g because they contain solutions. You can exclude using wildcards)

With these settings in place, whenever you commit updates on the main (private) source repo, the repo will be duplicated in the public repo (minus e.g the instructor files) and will be built using the `_toc.yml` and published on the Github pages branch. 

