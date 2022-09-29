# nordstream-leak
Climate implications of the NordStream pipeline leak in September 2022.

![Climate projections of NordStream pipeline leak](../plots/NordStream.png "NordStream")

## Pre-requisites
- `anaconda` (install from www.anaconda.org)
- `python` (v3.6 or later)
- `fair` v2.1-dev. This is currently unreleased - please contact me if you want access (twitter @chrisroadmap)

## Reproduction

1. Clone the repository to your local disk.
2. Create the `conda` environment with
```
conda env create -f environment.yml
```
3. Activate the environment with 
```
conda activate nordstream-leak
```
4. (optional) If you want to make nice version-control friendly notebooks, which will remove all output and data upon committing to GitHub, run
```
nbstripout --install
```
5. Start a `jupyter` console with
```
jupyter notebook
```
then navigate to the notebooks directory and run the notebooks.
