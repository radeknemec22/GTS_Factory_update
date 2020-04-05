# D2i Environments
Repository containing [Conda](https://docs.conda.io) environments (and relevant installation scripts) used in D2i ecosystem

| File						| Status     | Description                                                                                         	|
|-----------------------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| `.gitattributes`   				| 	     | Git attributes for Large File Storage (LFS)						 		|
| `_install_from_net.bat` 			| 	     | Installs environment with internet; arguments config.txt <env1> <env2> ...                               |
| `_install_from_packs.bat`   			| 	     | Installs environment with conda-packs; arguments config.txt <env1> <env2> ...                            |
| `_update_environment.bat`   			| 	     | Updates environment with internet; arguments config.txt <root/base> <env_name> [channel]                 |
| `config.txt`   				| 	     | Configuration containing Miniconda installation folder and latest environment numbers.       		|
| `create_D2iDeveloperV4-0_from_scratch.bat`	| 	     | Creates D2iDeveloperV4-0 with core packages (unversioned packages, so latest)                            |
| `create_D2iMinimalV4-0_from_scratch.bat`	| 	     | Creates D2iMinimalV4-0 with core packages (unversioned packages, so latest)                         	|
| `create_distribution.py`   			| deprecated | Creates redistributable conda bundles out of conda environments installed on the executing machine.	|
| `D2iDeveloperV3-1.yml`   			| deprecated | List of all packages in the D2iDeveloperV3-1 environment (Python 2)                                    	|
| `D2iDeveloperV3-2.yml`   			| deprecated | List of all packages in the D2iDeveloperV3-2 environment (Python 2)                             		|
| `D2iDeveloperV3-3.yml`   			| 	     | List of all packages in the D2iDeveloperV3-3 environment (Python 2)                             		|
| `D2iDeveloperV4-0.yml`   			| 	     | List of all packages in the D2iDeveloperV4-0 environment (Python 2)                             		|
| `D2iFixDevV1-0.yml.yml`   			| 	     | List of all packages in the D2iFixDevV1-0 environment (Python 3)                                		|
| `D2iMinimalV3-2.yml`   			| 	     | List of all packages in the D2iMinimalV3-2 environment (Python 2)                               		|
| `D2iMinimalV4-0.yml`   			| 	     | List of all packages in the D2iMinimalV4-0 environment (Python 3)                               		|
| `install_miniconda.bat`   			| broken     | Installs Miniconda                                        						|
| `install_python2_environment.bat`		| 	     | Installs D2iMinimal & D2iDeveloper environments with Python 2                                        	|
| `install_python2and3_environment.bat`		| 	     | Installs D2iMinimal & D2iDeveloper environments with Python 2 and 3                                      |
| `load_config.bat`   				| 	     | Loads config.txt                                       							|
| `netinstall_developer.bat`   			| deprecated | Installs (latest version of) algorithm execution environment                                        	|


## Install Miniconda
We currently have to versions of Miniconda:
- Miniconda2, conda v3.19.0 --> Python 2 only
- Miniconda3, conda v4.7.12 --> Python 2 and 3

Run the executable as administrator to install the version you need with the following options:
- Install for all users
- Add to path: yes
- Register Python: yes
- Install directory: C:\Miniconda*<br>

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