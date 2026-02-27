# Text Analysis for Social Scientists

## Using Google Colab (recommended)

For this course we recommend using [Google Colab](https://colab.research.google.com/), which allows you to run Jupyter Notebooks in your browser without installing anything. You just need a [Google account](https://support.google.com/accounts/answer/27441?hl=en).

### Python packages

The following Python packages are used in this course. Most are pre-installed in Google Colab; any additional packages are installed automatically at the top of each notebook:
* `nltk` - for natural language processing and text preprocessing
* `gensim` - for topic modelling (LDA)
* `wordcloud` - for generating word clouds
* `matplotlib` - for visualisation
* `pandas` - for data manipulation
* `scikit-learn` - for machine learning utilities
* `pyLDAvis` - for interactive topic model visualisation
* `requests` - for making HTTP requests

### R packages

If you are using the R notebooks, you will need to install the following packages (a code cell at the top of each R notebook handles this for you in Colab):
* `quanteda` - for text analysis
* `quanteda.textstats` - for text statistics
* `quanteda.textplots` - for text visualisation
* `topicmodels` - for topic modelling (LDA)
* `tidytext` - for tidy text mining
* `wordcloud2` - for generating word clouds
* `dplyr` - for data manipulation
* `ggplot2` - for visualisation
* `httr` - for making HTTP requests
* `jsonlite` - for working with JSON data
* `readr` - for reading data files
* `reshape2` - for reshaping data

## Installing Python

If you would like to download and install Python on your own machine:
* [How to Install Python on Windows 10](https://www.digitalocean.com/community/tutorials/install-python-windows-10)
* The above guide is relevant for installing on Mac also, just make sure you download the Mac version of Python: [https://www.python.org/downloads/macos/](https://www.python.org/downloads/macos/)

Once Python is installed, open your command prompt and run:

```
pip install nltk gensim wordcloud matplotlib pandas scikit-learn pyLDAvis requests
```

You will also need to download NLTK data. Open a Python shell and run:

```python
import nltk
nltk.download('punkt_tab')
nltk.download('stopwords')
nltk.download('wordnet')
```

## Installing R

If you would like to download and install R on your own machine:
* Download R from [https://cran.r-project.org/](https://cran.r-project.org/)
* Download RStudio (a user-friendly interface for R) from [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)

Once R is installed, open R and run:

```r
install.packages(c("quanteda", "quanteda.textstats", "quanteda.textplots", "topicmodels", "tidytext", "wordcloud2", "dplyr", "ggplot2", "httr", "jsonlite", "readr", "reshape2"))
```

## Running Jupyter Notebooks

You can run Jupyter Notebooks after installing Python by opening your command prompt and typing `jupyter lab`.

If it isn't installed on your machine yet then type `pip install jupyterlab` into your command prompt first and then type `jupyter lab`.

To run R in Jupyter Notebooks, you will need to install the IRkernel package. Open R and run:

```r
install.packages('IRkernel')
IRkernel::installspec()
```

## Troubleshooting

* **Package installation fails**: Try upgrading pip first with `pip install --upgrade pip`, then retry the install command.
* **NLTK data download errors**: Ensure you have an internet connection. If you are behind a firewall, you may need to configure proxy settings.
* **R package compilation errors on Windows**: Install [Rtools](https://cran.r-project.org/bin/windows/Rtools/) to enable compilation of packages from source.
* **R package compilation errors on Mac**: Install Xcode Command Line Tools by running `xcode-select --install` in your terminal.
* **Colab disconnects**: Google Colab sessions time out after a period of inactivity. Reconnect and re-run cells from the top of the notebook.
* **pyLDAvis not displaying**: Ensure you are running `pyLDAvis.enable_notebook()` before calling `pyLDAvis.display()`. In Colab, this should work automatically.
