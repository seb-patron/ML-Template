# My Python ML Project Template
This is my personal python machine learning project template that I use, based off the [medium one blog post here] [template].

# How to use
First, copy (don't git clone or else you need to overwrite settings later) this repository, enter terminal, and type:

$ conda env create -f environment.yml -n projectName

This creates an virtual enviroment with Anaconda. To activate it, type

$ source activate projectName

To update project with new packages, add them to environment.yml, then type in

$ conda env update -f environment.yml -n chaos

To start up Jupyter Notebooks type

$ jupyter notebook


[template]: https://medium.com/towards-data-science/structure-and-automated-workflow-for-a-machine-learning-project-2fa30d661c1e