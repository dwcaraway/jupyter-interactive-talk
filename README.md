# Talk: Building Interactive Visualization with Jupyter Notebook
This repository contains files for building interactive visualizations for the web using the Jupyter Notebook for scientific computing.

We utilize the Bokeh and Plotly libraries to generate the visualizations.

## Install Dependencies
Install dependencies with ``pip```.

```
pip install -r requirements.txt
```

## Install NBExtensions Javascript and CSS
The [Jupyter Notebook Extensions](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) add a lot of neat capabilities to Jupyter Notebook. The extensions are installed in the step above but we'll need to copy over the javascript and css libraries into your user directory and edits your configuration using the below command:
```
jupyter contrib nbextension install --user
```

You should now be able to edit your extensions at the Jupyter notebook home or by running the 'jupyter nbextension' command

## Configure ipywidgets
The IPyWidget provides a common widgets interface for interactivity in a Jupyter notebook. It's used for some of our examples and is required for the qgrid data viewer. To enable it, run:

```
jupyter nbextension enable --py --sys-prefix widgetsnbextension
```

## Virtual Environment Kernel
If you are using a virtualenv (highly recommended), you'll need to create a kernel specification to launch notebooks with it inside the Jupyter Notebook.


  mkdir -p ~/kernelspecs/vistalk
  jupyter kernelspec install ~/kernelspecs/vistalk --user


Afterwards, you'll need to relaunch any running jupyter notebook servers. Your kernel containing all the packings installed within your virtualenv are now available.

## Run the notebook
```
jupyter notebook
```

When the jupyter server launches, a browser window will open to the server. The URL to access the server will be displayed in the terminal along with a token (if using default config) required to discourage CSRF attacks.

## Animations
To run the animations and interactive plots for bokeh, you'll want to run a bokeh server concurrently in the background. You can do so by invoking

  bokeh serve
