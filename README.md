# Spatial Data Analysis with PySAL @FOSS4G
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sjsrey/pysalfoss4g19/master)

### Instructors

- [Sergio Rey](http://sergerey.org) - University of California, Riverside
- [Wei Kang](http://spatial.ucr.edu/peopleKang.html) - University of California, Riverside
- [Elijah Knaap](http://spatial.ucr.edu/peopleKaap.html) - University of California, Riverside
- [Stefanie Lumnitz](https://github.com/slumnitz) - University of British Columbia
---

This repository contains the materials and instructions for the PySAL workshop at [FOSS4G 2019](https://2019.foss4g-na.org/).


## Schedule (Proposed)


* 2:00-3:30
  * PySAL Overview
  * Spatial data processing
  * Spatial weights
  * Choropleth mapping and geovisualization
* 3:30-4:00
  * Break
* 4:00-5:30
  * Global spatial autocorrelation
  * Local spatial autocorrelation
  * Spatial dynamics
  
## Obtaining Workshop Materials

If you are familiar with GitHub, you should clone or fork this GitHub repository to a specific directory. Cloning can be done by:

```bash
git clone https://github.com/sjsrey/pysalfoss4g19.git
```

If you are not using git, you can grab the workshop materials as a zip file by pointing your browser to (https://github.com/sjsrey/pysalfoss4g19.git) and clicking on the green *Clone or download* button in the upper right.

![download](figs/readmefigs/download.png)

Extract the downloaded zip file to a working directory.

## Installation

We will be using a number of Python packages for geospatial analysis.


An easy way to install all of these packages is to use a Python distribution such as [Anaconda](https://www.anaconda.com/download/#macos). In this workshop we will use anaconda to build an [environment](https://conda.io/docs/user-guide/tasks/manage-environments.html) for **Python 3.6**. It does not matter which version of anaconda is downloaded. We recommend installing Anaconda 3.7.

![anaconda](figs/readmefigs/anaconda.png)


On windows, all our work will begin from an anaconda prompt, which you can start as follows:

![anacondaprompt](figs/readmefigs/anacondastartwin.png)

Start a terminal and navigate to the directory of the downloaded/ cloned materials. For example, if the materials now live in the directory ```/Users/weikang/Downloads/pysalnarsc18-master```, you need to navigate to that directory from the terminal (using command ```cd```):

![directory](figs/readmefigs/directory.png)

Once we have done that, run:

```bash
conda-env create -f workshop.yml
```

This will build a conda python 3.6 environment that sandboxes the installation of the required packages for this workshop so we don't break anything in your computer's system Python (if it has one).

This may take 10-15 minutes to complete depending on the speed of your network connection.

Once this completes, you can activate the workshop environment with:

* on Mac, Linux
```bash
source activate workshop
```
* on Windows:
```bash
activate workshop
```

Next, you will want to test your installation with:
```bash
 jupyter-nbconvert --execute --ExecutePreprocessor.timeout=120 check_workshop.ipynb
```

You should see something like:
```bash
[NbConvertApp] Converting notebook check_workshop.ipynb to html
[NbConvertApp] Executing notebook with kernel: python3
[NbConvertApp] Writing 347535 bytes to check_workshop.html
```

Open check_workshop.html in a browser, and scroll all the way down, you should see something like:

![htmlout](figs/readmefigs/htmlout.png)

You should also see a new file in the current directory called `inc.png` that contains a map looking something line:

![incmap](figs/readmefigs/inc.png)

If you do see the above, you are ready for the tutorial. If not, please contact either of us for help.

## Troubleshooting


If you encounter the following error when starting jupyterlab:
```bash
FileNotFoundError: [WinError 2] The system cannot find the file specified
```
A solution is to issue the following command in the anaconda prompt:
```bash
 python -m ipykernel install --user
```

