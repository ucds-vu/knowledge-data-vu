# Python

A working version of Python 3 is needed for this course. Below are instructions to help you install and setup Python 3 on your device. Contact an TA if you run into problems.

## Installation

There is a good chance that Python is already installed on your system. You can check this by opening a terminal (Linux/Mac) or powershell (Windows) and executing the follow command:

    python --version

If this command cannot be found, or if the returned version is less than `3.10`, then you will need to install the latest release of Python yourself. Linux users can do so by running their distribution's package manager, looking up Python 3 and installing/updating it from there, or by [downloading the tarball and compiling Python 3 from source](https://www.python.org/downloads/source/). Windows and Mac users can download and run the Python 3 installer for [Windows](https://www.python.org/downloads/windows/) or [Mac](https://www.python.org/downloads/macos/), respectively. **Be sure to select the option to add Python to `PATH`** if asked.

Verify whether Python 3 has successfully been installed by running the `python --version` command once more. You may need to restart your device.

## Virtual Environment

It is recommended to work from a [virtual environment](https://docs.python.org/3/library/venv.html). Virtual environments mimic your system-wide Python installation but enable you to install 3rd-party libraries that are only accessible from within a specific virtual environment. This avoids the need to install such libraries on a system-wide scale and makes it easier to run different versions of the same library. 

Open a terminal or powershell and traverse, using `cd`, to a suitable directory to create the virtual environment in. Once inside the preferred directory, execute the following command:

    pythom -m venv python_venv

This creates a new directory called `python_venv` in which your virtual environment resides. Note that the virtual environment now only has been created; to actually use it we first have to activate it, which can be done via the following command:

For Linux/Mac users:

    source python_venv/bin/activate

For Windows users:

    python_venv\Scripts\Activate.ps1

That's it! Everything Python-related you will now do in this terminal or powershell will be run within the virtual environment. To now exit this environment, and to return to the system-wide Python environment, you'll need to the following command:

    deactivate

Be aware that you will need to active the virtual environment each time you restart your device or open another terminal/powershell. Forgetting this will put you in the system-wide Python environment.

## Installing Libraries

You will need to install several 3rd-party libraries for this course. Most of these are installed automatically, but you still need to install one library yourself to properly set you up for the course assignments. To do so, we are going to use [pip](https://pip.pypa.io/en/stable/installation/), the Python package manager.

First, ensure that you are in the terminal or powershell in the course directory, and that the virtual environment has been activated. You are now going to install `jupyterlab`, which is an interactive Python notebook which can be edited from your webbrowser. To install `jupyterlab`, run the following command:

    pip install jupyterlab

or

    pip3 install jupyterlab

This will download and install the library and all its dependencies. Once completed, you are set to go. While the course also uses other 3rd-party libraries, these are automatically installed from the `jupyterlab` notebooks when needed.

## JupyterLab

Interactive notebooks are simple and effective tools for testing small bits of your code before you integrate it in a larger application. We will use [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html) in this course.

First, ensure that you are in the terminal or powershell in the course directory, and that the virtual environment has been activated. Run the following command to start JupyterLab:

    jupyter-lab

Wait a few seconds for the program to start. Next, open your webbrowser and go to `127.0.0.1:8888` to access the web interface. You can now load notebook files (`.ipynb`) from the left pane. Be aware that the root of the file browser pane is the same directory as that you ran the above command from. If you cannot see your notebook files (and you are sure they are there) try restarting JupyterLab from a higher directory.

