clean:
	rm -f data/raw/*.csv
	rm -f data/processed/*.pickle
	rm -f data/processed/*.xlsx
	rm -f reports/figures/*.png

# replace with desired output dest and name, and url with download source
URL = "https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data"

data/raw/source.csv:
	python data/download.py $(URL) $@

data/processed/processed.pickle: data/raw/source.csv
	python data/preprocess.py $< $@ --excel data/processed/processed.xlsx

reports/figures/exploratory.png: data/processed/processed.pickle
	python visualization/exploratory.py 
	data/processed/processed.pickle 
	reports/figures/exploratory.png

all: data/processed/processed.pickle reports/figures/exploratory.png