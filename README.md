# template-jupyter-project
Template to use for new python-based Jupyter notebook projects

## First steps

This assumes that you are developing with `conda` and `python` 3.7, 3.8 or 3.9. These instructions should work for Windows when using Anaconda Prompt and for MacOS in Terminal (and by extension, likely will work on Linux).

1. Edit the `environment.yml` file:
  - Uncomment the `name` attribute.
  - After `name`, enter the name you want for your environment. Good practice is to use the same name for the environment as for the repo.
  - Edit the dependencies list as required.
2. Create your environment:

```
conda env create -f environment.yml
```
3. If you want to make nice version-control friendly notebooks, which will remove all output and data upon committing, run
```
nbstripout --install
```

4. Examine .gitignore and decide where you want to put any large input or output datasets that you don't want to commit to GitHub, and fill in these paths.

## Operation 

### Developing your package

Most of the time your workflow will look like this

```
conda activate your-env-name
jupyter notebook
```

### Updating requirements

As you build the package you will likely want to add more dependencies. Edit the `environment.yml` file and run
```
conda env update -f environment.yml --prune
```

Please do not overwrite the `environment.yml` file using `conda env export`, as this exports everything in your local environment including all sub-dependencies and OS-specific packages (and sometimes local paths).
