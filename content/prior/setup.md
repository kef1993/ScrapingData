In this tutorial, you will set up a scientific Python computing environment using the [Anaconda python distribution by Continuum Analytics](https://www.continuum.io/downloads).

## Why Python?
As is true in human language, there are hundreds of computer programming languages. While each has its own merit, the major languages for data science are Python and R. Both are good to know. Python has historically been more prominent outside of academia and for processing web data. Some cutting-edge statistical functions are only available in R libraries, while the most popular machine learning algorithms are likely to have more established Python libraries. Both are open source. Python code syntax can typically be read as if they were written in plain english, which makes the languages a useful tool for teaching and learning. but it is also very powerful language that is actively used in real-life research.



## Installing Python 3.7 with Anaconda

There are several scientific Python distributions available for MacOS, Windows, and Linux. The  most popular, [Anaconda](https://www.continuum.io/why-anaconda), is specifically designed for scientific computing and data science work. For this course, we will use the Anaconda Python 3.7 distribution. To install the correct version, follow the instructions below.
1. Navigate to the [Anaconda download page](https://www.anaconda.com/distribution/#download-section) and download the Python 3.7 graphical installer.
2. Launch the installer and follow the onscreen instructions.
3. Congratulations! You now have the beginnings of a scientific Python distribution.


## Installing additional packages
With the Anaconda Python distribution, you can install verified packages (scientific and non-scientific) through the Conda package manager. Note that you do not have to download Conda separately. This comes packaged with Anaconda. To install packages through Conda, we must manually enter their names on the command line.

1. Open  a prompt.
   1. To open a terminal on OSX, click on the search icon in the upper right-hand corner of your menu bar and type "Terminal". This application is installed by default on your computer.

   2. On Windows,  press the “Windows Key” and on the search bar write “Anaconda Prompt”.
2. To make sure your package manager is up to date, type "conda update conda" and return. Note that you will have to type `y` in your terminal when prompted. This is to ensure that you are aware of what is being installed and what dependencies it requires.
3. To make sure all your packages are up to date, type `conda update anaconda` and return.

When a library is not available through conda, you can use `pip`, a package manager with a larger number of libraries but limited to Python.  The syntax for pip is similar. For example, typing `pip install [x]` in the terminal will install the [x] library.









Note: This is a modified version of Griffin Chure's [Setting Up Python For Scientific Computing](http://bi1.caltech.edu/code/t0a_setting_up_python.html). This work is licensed under a [Creative Commons Attribution License CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).
