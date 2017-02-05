# Talk: Building Interactive Visualization with Jupyter Notebook
This repository contains files for building interactive visualizations for the web using the Jupyter Notebook for scientific computing.

We utilize the Bokeh and Plotly libraries to generate the visualizations.

## Install Dependencies
Install dependencies with ``pip```.

```
pip install -r requirements.txt
```

## Install NBExtensions Javascript and CSS
We use the [Jupyter Notebook Extensions](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) to create a table of contents. The extensions are installed in the step above but we'll need to copy over the javascript and css libraries into your user directory and edits your configuration using the below command:
```
jupyter contrib nbextension install --user
```

There are lots of great extensions for Jupyter in this library. Let's enable the Table of Contents extension:
```
jupyter nbextension enable toc2/main
```

## Install and configure NBPresent
We use NBPresent to run our Jupyter notebook as a slide show
```
jupyter nbextension install nbpresent --py --overwrite
jupyter nbextension enable nbpresent --py
jupyter serverextension enable nbpresent --py
```

## Configure ipywidgets
```
jupyter nbextension enable --py --sys-prefix widgetsnbextension
```

## Virtual Environment Kernal
If you are using a virtualenv, see [notes for creating a kernal](https://help.pythonanywhere.com/pages/IPythonNotebookVirtualenvs/)

## Run the notebook
```
jupyter notebook
```


