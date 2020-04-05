# GTS Factory update - environment & script
Repository containing [Miniconda3](https://docs.conda.io) environment used for GTS Factory update script.

## Install Miniconda
- Miniconda3, conda v4.7.12 --> Python 2 and 3

Run the executable (Miniconda3-4.7.12-Windows-x86_64.exe) as administrator to install Miniconda with following options:
- Install for: All users
- Install directory: C:\Miniconda3
- Add Anaconda to the system PATH: yes
- Register Anaconda as the system Python 3.7: yes

## Install conda environment
Conda environtments can either be installed with the batch-files of manually.

### With batch file
Not supported yet.

### Manual installation and activation
To install environments manually, open command line as administrator and navigate to the directory with .yml file
- Install with internet
	- To create new environment, use the following command:
	  conda env create --name GTSAutomation --file environment.yml
	  (conda env create --name \<name\> --file \<name\>.yml)

	- To activate the environment, use the following command:
	  conda activate GTSAutomation
	  (conda activate \<env_name\>)

- Install with conda-pack (distributable)
	- See https://conda.github.io/conda-pack/

## How to use the script
Will be added later.
