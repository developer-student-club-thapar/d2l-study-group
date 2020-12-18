# Installation
:label:`chapter_installation`

To get you up and running with hands-on experiences, we'll need you to set up with a Python environment, Jupyter's interactive notebooks, the relevant libraries, and the code needed to *run the book*.

## Obtaining Source Code

The source code package containing all notebooks is available at https://github.com/developer-student-club-thapar/d2l-study-group.git Please clone it into your working folder.

```
git clone https://github.com/developer-student-club-thapar/d2l-study-group.git
```

## Installing Miniconda

The simplest way to get going will be to install
[Miniconda](https://conda.io/en/latest/miniconda.html). The Python 3.x version
is required. You can skip the following steps if conda has already been installed.
Download the corresponding Miniconda sh file from the website
and then execute the installation from the command line
using `sh <FILENAME> -b`. For macOS users:

```bash
# The file name is subject to changes
sh Miniconda3-latest-MacOSX-x86_64.sh -b
```


For Linux users:

```bash
# The file name is subject to changes
sh Miniconda3-latest-Linux-x86_64.sh -b
```


Next, initialize the shell so we can run `conda` directly.

```bash
~/miniconda3/bin/conda init
```


Now close and re-open your current shell. You should be able to create a new
environment as following:

```bash
conda create --name d2l python=3.8 -y
```

Now we will want to activate the `d2l` environment.

```bash
conda activate d2l
```

## Installing the Framework and the `d2l` Package

:begin_tab:`pytorch`

```bash
pip install torch torchvision -f https://download.pytorch.org/whl/torch_stable.html
```


:end_tab:

:begin_tab:`tensorflow`
You can install TensorFlow with both CPU and GPU support via the following:

```bash
pip install tensorflow tensorflow-probability
```


:end_tab:


We also install the `d2l` package that encapsulates frequently used
functions and classes in this book.

```bash
# -U: Upgrade all packages to the newest available version
pip install -U d2l
```


Once they are installed, we now open the Jupyter notebook by running:

```bash
jupyter notebook
```


At this point, you can open http://localhost:8888 (it usually opens automatically) in your Web browser. Then we can run the code for each section of the book.
Please always execute `conda activate d2l` to activate the runtime environment
before running the code of the book or updating the deep learning framework or the `d2l` package.
To exit the environment, run `conda deactivate`.

