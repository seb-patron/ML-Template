clean:
	rm -f data/raw/*.csv

# replace with desired output dest and name, and url with download source
URL = "https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data"

data/raw/source.csv:
	python data/download.py $(URL) $@

all: data/raw/source.csv