# Use Binder to Write and Run Your Jupyter Notebook

Binder is a tool that lets other people easily launch an interactive copy of your Jupyter notebooks. 

- [Binder Homepage](https://mybinder.org/)

- [Binder Documentation](https://mybinder.readthedocs.io/en/latest/)


## Conda environment with environment.yml

[![Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/EvanLi/run-jupyter/master/?filepath=example.ipynb)

A Binder-compatible repo with an `environment.yml` file.

Access this Binder at the following URL:

https://mybinder.org/v2/gh/EvanLi/run-jupyter/master

Access the example.ipynb file at the following URL:

https://mybinder.org/v2/gh/EvanLi/run-jupyter/master/?filepath=example.ipynb

## Notes
The `environment.yml` file should list all Python libraries on which your notebooks
depend, specified as though they were created using the following `conda` commands:

```
source activate example-environment
conda env export --no-builds -f environment.yml
```

Note that the only libraries available to you will be the ones specified in
the `environment.yml`, so be sure to include everything that you need! 

Also note that conda will possibly try to include OS-specific packages in `environment.yml`, so you
may have to manually prune `environment.yml` to get rid of these packages. Confirmed Mac-OSX-specific
packages that should be removed are:

* libcxxabi=4.0.1
* appnope=0.1.0
* libgfortran=3.0.1
* libcxx=4.0.1

## Packages already installed:

```
dependencies:
  - beautifulsoup4
  - bokeh
  - catboost
  - dask
  - dill
  - eli5
  - lxml
  - matplotlib
  - numpy
  - pandas
  - partd
  - psutil
  - requests
  - scikit-learn
  - scipy
  - seaborn
  - toolz
```

You can use this command in jupyter notebook to install the packages in requirements.txt:

```
!pip install -r requirements.txt
```

Or just install what you need:

```
!pip install package_name
```