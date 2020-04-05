# GTS Factory update - environment & script
Repository containing [Miniconda3](https://docs.conda.io) environment used for GTS Factory update script.

## Install Miniconda
- Miniconda3, conda v4.7.12 --> Python 2 and 3

Run the executable as administrator to install Miniconda with following options:
- Install for: All users
- Install directory: C:\Miniconda3
- Add Anaconda to the system PATH: yes
- Register Anaconda as the system Python 3.7: yes

## Install conda environment
Conda environtments can either be installed with the batch-files of manually.

### With batch file
Not supported yet.

### Manual installation
To install environments manually, open command line as administrator.
- Install with internet
	- To create new environment, use one of the following commands:
 	  conda env create --name \<name\> --file \<name\>.yml

	- To update and environment (e.g. root/base (= \<name\>)), use one of the following commands:
	  conda env update --name \<name\> --file \<filename\>.yml

- Install with conda-pack (distributable)
	- See https://conda.github.io/conda-pack/
