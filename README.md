# GTS Factory update - environment & script
Repository containing [Miniconda3](https://docs.conda.io) environment used for GTS Factory update script.

## Install Miniconda
- Miniconda3, conda v4.7.12 --> Python 2 and 3

Run the executable as administrator to install the version you need with the following options:
- Install for all users
- Add to path: yes
- Register Python: yes
- Install directory: C:\Miniconda3<br>

\* If you install Miniconda elsewhere, change the location in the config.txt file.

## Install conda environment
Conda environtments can either be installed with the batch-files of manually.
Note that v3-x are Python 2 and v4-x are Python 3 environments.

### With batch file
- Run "install_python2_environment.bat config.txt" in cmd (as administrator)<br>
  This will install Python 2 for Miniconda2, that means the following environments:<br>
	D2iMinimalV3-2<br>
	D2iDeveloperV3-3<br>
	Clones D2iDeveloperV3-3 to root
- Run "install_python2and3_environment.bat config.txt" in cmd (as administrator)<br>
  This will install Python 2 and 3 for Miniconda3, that means the following environments:<br>
        D2iMinimalV3-2<br>
        D2iDeveloperV3-3<br>
        D2iMinimalV4-0<br>
        D2iDeveloperV4-0<br>
        Clones D2iDeveloperV4-0 to base

### Manual installation
To install environments manually, open command line as administrator.
- Install with internet
	- To create new environment, use one of the following commands:<br>
 	  conda env create --name \<name\> --file \<name\>.yml<br>
	  or<br>
      conda create --name \<name\> --file \<name\>.condaenv [-c \<channel\>]

	- To update and environment (e.g. root/base (= \<name\>)), use one of the following commands:<br>
	  conda env update --name \<name\> --file \<filename\>.yml<br>
	  or<br>
	  conda install --name \<name\> --file \<filename\>.condaenv [-c \<channel\>]

- Install with conda-pack (distributable)
	- See https://conda.github.io/conda-pack/
