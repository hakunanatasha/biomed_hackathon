### Biomedical datasets hackathon

The formal guide to creating a shared dataset is [here](https://huggingface.co/docs/datasets/share_dataset.html), but we will walk you through the process here. 

Official instructions for how to implement a dataset in 🤗 exists [here](https://huggingface.co/docs/datasets/add_dataset.html). 

Please make a github account prior to implementing a dataset; install `git` and additionally `git lfs`, as the latter is required for transferring larger files. Installation instructions are below:

Installation: <br>
    - [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) <br>
    - [git-lfs](https://git-lfs.github.com/) <br>

If you choose to fork the repo, you will likely require the following: <br>
    - [flake8 linter](https://flake8.pycqa.org/en/latest/) <br>
    - [isort](https://github.com/PyCQA/isort) <br>
    - [black](https://black.readthedocs.io/en/stable/) <br>

These can be installed if you run `pip install -r requirements.txt` within the datasets repository *ideally in your own python environment*.

## Option 1: Fork from the datasets repo and make a dataset "manually"

### 1. **Assign yourself a dataset**

Check if the dataset already exists in the 🤗 [Hub](https://huggingface.co/datasets) OR look to see if there is an issue on the biomedical data science repository [here](https://github.com/bigscience-workshop/biomedical/issues).

If the dataset does not exist OR if an issue is open (there are no people assigned to the issue) please feel free to assign yourself to the issue. To do so, make a comment on the issue that you would like to take this dataset, and an organizer will add you to the repo.

### 2. **Setup a local version of the datasets repo to update**
Fork the dataset [repository](https://github.com/huggingface/datasets) from huggingface to your local github account. 

After you fork, clone the repository locally. You can do so as follows:

    git clone https://github.com/<your_github_username>/
    cd datasets  # enter the directory

Next, you want to set your `upstream` location to enable you to push/pull (add or receive updates). You can do so as follows:
    
    git remote add upstream https://github.com/huggingface/datasets.git

You can optionally check that this was set properly by running the following command:
    
    git remote -v 

You should note an `origin` pointing to your fork, and an `upstream` pointing to the official 🤗 repository. If you do NOT have an `origin` for whatever reason, then run:

    git remote add origin https://github.com/<your_github_username>/datasets.git

Finally, make a custom branch to implement your changes. You can make a new branch as such:

    git checkout -b <name_of_my_dataset>

**Please do not make changes on the master branch!** Always make sure you're on the right branch by checking:

    git branch

### 3. **Create a development environment** 
You can also make an alternative environment to test changes.** You may do this however you choose, but the 🤗 option is:

`   pip install -e ".[dev]"`

If you make your own environment, be sure to run `python setup.py install` within the datasets repository to ensure you have all necessary packages.

**Note! If you already have the `datasets` library installed in your environment of choice, please uninstall (via `pip uninstall datasets`) and re-install in the editable mode**

### 4. **Implement your dataset**

Make a new directory within the `datasets` folder as such: <br>

    mkdir datasets/<name_of_my_dataset>
    cd datasets/<name_of_my_dataset>

Implement your dataset following the guide in `template.py`.

### 5. **Format code** via the following commands:

    make style
    make quality

This runs the black formatter, isort, and lints to ensure that the code is readable and looks nice. Flake8 linting errors may require manual changes.

### 6. **Commit your changes** now you're ready to submit your new dataset!

First, commit your changes to the branch to "add" the work:

    git add datasets/<name_of_my_dataset>
    git commit

*Ideally, run* `git commit -m "A message of your commits"`

Then, run the following commands to incorporate any new changes in the master branch of datasets as follows:

    git fetch upstream
    git rebase upstream/master

**Run these commands in your custom branch**.

Push these changes to **your fork** with the following command:

    git push -u origin <name_of_my_dataset>

**[Optional Step]** Add unit-tests and meta data by following instructions [here](https://huggingface.co/docs/datasets/share_dataset.html#adding-tests).

### 7. **Make a pull request** 

Make a PR to implement your changes on the main repository [here](https://github.com/huggingface/datasets/pulls). To do so, click "New Pull Request". Then, choose your branch from your fork to push into "base:master".

