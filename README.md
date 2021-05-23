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

Put on gh-pages branch

```
ghp-import -n -p -f _build/html
```

To change the footer edit the `<a>` tags in `_config.yml`. 

The toc needs to be structured as in order for the styling to work correctly

``` yaml
- file: intro
- part: Chapter Headline 
  chapters:
    - file: markdown
    - file: notebooks

```
