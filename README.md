# GTS Factory update - environment & script
Repository containing [Miniconda3](https://docs.conda.io) environment used for GTS Factory update script.

## Install Miniconda
- Miniconda3, conda v4.7.12 --> Python 2 and 3

Run the executable (Miniconda3-4.7.12-Windows-x86_64.exe) as administrator to install Miniconda with following options:
- Install for: All users
- Install directory: C:\Miniconda3
- Add Anaconda to the system PATH: yes
- Register Anaconda as the system Python 3.7: yes

## Environment installation and activation
To install environments manually, open command line as administrator and navigate to the directory with .yml file
- Install with internet
	- To create new environment, use the following command:<br>
	  conda env create --name GTSAutomation --file environment.yml<br>
	  (conda env create --name \<name\> --file \<name\>.yml)

	- To activate the environment, use the following command:<br>
	  conda activate GTSAutomation<br>
	  (conda activate \<env_name\>)
	  
	- For more information [CLICK HERE](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#removing-an-environment)

- Install with conda-pack (distributable)
	- See https://conda.github.io/conda-pack/
	

## How to use the script
Will be added later.

To run the script, open command line as administrator and navigate to the directory with the files and execute following commands:<br>
conda activate GTSAutomation<br>
jupyter-notebook<br>

