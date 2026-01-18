# PSYC 599: Computational Language Neuroscience
This repository accompanies the USC graduate course "Computational Language Neuroscience" created by Samuel A. Nastase ([course website](https://snastase.github.io/teaching/psyc599)). The `readings/` folder contains PDFs of the weekly readings and the `labs/` folder contains Jupyter Notebooks comprising the interactive lab exercises.

## Setting up your computing environment
To work through the Jupyter Notebooks, I recommend setting up a dedicated computing environment for this class using [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). You can set up this conda environment locally (on your laptop) or remotely (e.g., on your lab or institutional server). If your computer doesn't already have conda, you can install [miniconda](https://docs.conda.io/en/latest/miniconda.html). (If you already have a working conda installation, you can skip this step.)

If you're on an Apple Silicon (M-series) Mac, run the following code and confirm (yes) the prompts:

```
cd ~
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
bash Miniconda3-latest-MacOSX-arm64.sh
```

If you're on a Linux machine or a Windows machine, follow the corresponding [installation instructions](https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions).

Next, we'll create a conda environment for the class and activate that environment.

```
conda create --name psyc599
conda activate psyc599
```

You should now be able to see `(psyc599)` on your command-line prompt, indicating that the `psyc599` environment is active.

Now we'll install some necessary packages (and their dependencies) into our conda environment.

```
conda install -c conda-forge jupyterlab scipy matplotlib seaborn pytorch mne-base git gh
```

Finally, we'll install nilearn using pip just to play it safe.

```
pip install nilearn
```

Later in the course, we may some additional packages—but don't worry about this for now. Make sure to activate your conda environment if it's not already active (`conda activate psyc599`) whenever you start working on the notebooks.

**What's the point of all this?** Setting up a dedicated software environment (e.g., using [conda](https://docs.conda.io/), [Docker](https://www.docker.com/)) is a good practice for improving the reproducibility of your science. The goal of using conda here is to encapsulate the software you're using for this class (from other software on your computer) and explicitly track the versions of the software you use. In a perfect world, at the end of this course (or even years later), you could look back at your environment and reconstruct exactly what software you used for your analyses and even share that exact software environment with other scientists. I recommend setting up dedicated software environments like this for your major research projects as well.

## Working on the lab notebooks
The Jupyter Notebooks for lab are hosted on this GitHub repository. If you navigate to the notebook file (e.g., [`lab-1-localizer.ipynb`](https://github.com/snastase/psyc599/blob/main/labs/lab-1-localizer.ipynb)), you can click the "Download raw file" button to download the notebook.

Alternatively, you can use git to clone the entire repository. (Navigate to a directory where you want to store the class readings/code before running this command.)

```
git clone https://github.com/snastase/psyc599.git
cd psyc599
```

When you want to download new labs or updates to the GitHub repository, navigate to your local clone of the repo and pull the changes.

```
git pull
```

**Important!** Before you start working on a notebook, create a copy of the file with a new filename including your own name (e.g., `cp lab-1-localizer.ipynb lab-1-localizer-sam.ipynb`). This will help avoid filename collisions in git and will make it easier for me to grade your notebooks.

To start working on a notebook, activate your conda environment, navigate to the directory containing the notebooks (or your clone of the repo), and run Jupyter Lab.

```
jupyter lab
```

This will open an interactive development environment in your browser where you should be able to open and run the notebooks.

If you run into any problems, ***ask questions early and often!***
