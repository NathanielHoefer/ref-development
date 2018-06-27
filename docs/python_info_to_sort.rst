===============================================================================
Python Info To Sort
===============================================================================

.. contents:: Table of Contents

===============================================================================
Pip
===============================================================================
Tool used for installing python packages

Operations
**********
- :ref:`Installing a package`
- :ref:`Removing a package`
- :ref:`List all installed packages`
- :ref:`Get info on a specific package`
- :ref:`Search for a package`
- :ref:`Storing project dependencies`
- :ref:`Install all packages listed in requirements.txt`

Resources
*********
- Python Packaging User Guide (https://packaging.python.org/)
- Pip (http://pip.readthedocs.org/en/latest/index.html)
- Python Package Index (PyPI) (http://pypi.python.org)

Commands
********
.. code-block:: bash
    :caption: Installing a package
    :name: Installing a package

    pip install <package>
    pip install <package>==1.0
    pip install '<package>>=2.1'

.. code-block:: bash
    :caption: Removing a package
    :name: Removing a package

    pip uninstall <package>

.. code-block:: bash
    :caption: List all installed packages
    :name: List all installed packages

    pip list

.. code-block:: bash
    :caption: Get info on a specific package
    :name: Get info on a specific package

    pip show <package>

.. code-block:: bash
    :caption: Search for a package
    :name: Search for a package

    pip search <query>

.. code-block:: bash
    :caption: Storing project dependencies
    :name: Storing project dependencies

    pip freeze > requirements.txt

.. code-block:: bash
    :caption: Install all packages listed in requirements.txt
    :name: Install all packages listed in requirements.txt

    pip install -r requirements.txt


===============================================================================
Virtual Environments
===============================================================================
Isolated Python environments that can be entered and exited to avoid dependency conflicts between projects.

When working with virtual environments, use the virtualenvwrapper as it provides easier tools for managing virtual environments.

Quickstart
**********
:ref:`Quickstart commands to setup virtual environments`

Virtualenv
**********
The default tool used for creating virtual environments.

Operations
^^^^^^^^^^
- :ref:`Installing virtualenv`
- :ref:`Creating new virtualenv`
- :ref:`Enter virtual environment`
- :ref:`Exit virtual environment`
- :ref:`Checking python executable path`

Notes
^^^^^
- Usual directory for virtualenvs: `~/.virtualenvs`
- You should see (<env-name>) to the left of the terminal prompt when in a virtual environment.

Virtualenvwrapper
*****************
A user-friendly wrapper around virtualenv

Operations
^^^^^^^^^^
- :ref:`Installing virtualenvwrapper`
- :ref:`List virtual environments via Wrapper`
- :ref:`Enter virtual environment and switch to project via Wrapper`
- :ref:`Create and remove virtual environment via Wrapper`
- :ref:`Couple project dir with virtual environment`
- :ref:`Create project from scratch`: Creates virtual environment, project directory, and binds them together

Resources
^^^^^^^^^
- Virtualenv (https://virtualenv.pypa.io/en/stable)
- Virtualenvwrapper (http://virtualenvwrapper.readthedocs.io/en/latest/)
- Virtualenvwrapper-win (https://pypi.org/project/virtualenvwrapper-win/)


Virtual Environment Commands
****************************
.. code-block:: bash
    :caption: Quickstart commands to setup virtual environments
    :name: Quickstart commands to setup virtual environments

    # Change as necessary
    VENV_PATH="/usr/local/bin/virtualenvwrapper.sh"
    PROJ_PATH="$HOME/dev"

    sudo pip install virtualenv
    sudo pip install virtualenvwrapper
    echo "source $VENV_PATH" >> ~/.profile
    echo "export PROJECT_HOME=$PROJ_PATH" >> ~/.profile
    . ~/.profile

.. code-block:: bash
    :caption: Installing virtualenv
    :name: Installing virtualenv

    sudo pip install virtualenv

.. code-block:: bash
    :caption: Creating new virtualenv
    :name: Creating new virtualenv

    virtualenv <env-name>

.. code-block:: bash
    :caption: Enter virtual environment
    :name: Enter virtual environment

    . ~/.virtualenvs/<env-name>/bin/activate

.. code-block:: bash
    :caption: Exit virtual environment
    :name: Exit virtual environment

    deactivate

.. code-block:: bash
    :caption: Checking python executable path
    :name: Checking python executable path

    which python
    output: /path/path/bin/python

.. code-block:: bash
    :caption: Installing virtualenvwrapper
    :name: Installing virtualenvwrapper

    Unix:
    (sudo) pip install virtualenvwrapper
     # Add the following to ~/.profile
        source /usr/local/bin/virtualenvwrapper.sh
        export PROJECT_HOME="$HOME/<dev path>"
     . ~/.profile  # To reload profile file
     # Default virtualenv location: ~/.virtualenvs

    Windows:
    pip install virtualenvwrapper-win
    # Default virtualenv location: %USERPROFILE%\Envs

.. code-block:: bash
    :caption: List virtual environments via Wrapper
    :name: List virtual environments via Wrapper

    workon

.. code-block:: bash
    :caption: Enter virtual environment and switch to project via Wrapper
    :name: Enter virtual environment and switch to project via Wrapper

    workon <env-name>

.. code-block:: bash
    :caption: Create and remove virtual environment via Wrapper
    :name: Create and remove virtual environment via Wrapper

    mkvirtualenv <env-name>
    rmvirtualenv <env-name>

.. code-block:: bash
    :caption: Couple project dir with virtual environment
    :name: Couple project dir with virtual environment

    Unix:
    workon <env-name>  # Ensure currently in virtual environment
    cd /path/to/project
    setvirtualenvproject

    Windows:
    workon <env-name>  # Ensure currently in virtual environment
    cd \path\to\project
    setprojectdir

.. code-block:: bash
    :caption: Create project from scratch
    :name: Create project from scratch

    mkproject <project-name>
    # Not available in Windows
