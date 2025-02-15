# I Open at the Close: A Deep Reinforcement Learning Evaluation of Open Streets Initiatives

Code, data, and figures for our [paper](https://arxiv.org/abs/2312.07680).

### Code

All code for the paper appears in the `code` folder.

### Data

The data sources we use (listed below) tend to be quite large. We preprocessed a bunch of them and saved them in the `data` folder.

### Flows

The taxi data set is particularly large. We load each individually and infer routes using Dijkstra's weighted shortest path algorithm. Then the total traffic on edge edge in the road network is saved to the `flows` folder.

### Saved Models

Many of our models took substantial resources to train. We generally saved their weights in the `saved_models` folder.

### Figures

We made one several pretty figures of Q values in Manhattan according to our deep Q GNN. You should check it out! Some of these figures are not up to date with the what we included in the paper.

### Data Sources

• [NYC Collisions](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)

• [NYC Lion](https://www.nyc.gov/site/planning/data-maps/open-data/dwn-lion.page)

• [NOAA Daily Weather Data](https://www.ncdc.noaa.gov/cdo-web/datatools)

• [NYC Taxi Data](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

#### Installation notes
If you have issues installing torch-sparse, torch-scatter and/or pyg-lib, check your torch version by running `python`, `import torch`, then `torch.__version__`. Once you exit the python environment, uninstall the current versions by running `pip uninstall torch-scatter torch-sparse pyg-lib`. Then, if your torch version is `2.0.1+cu117` run `pip install torch-scatter torch-sparse pyg-lib -f https://data.pyg.org/whl/torch-2.0.1+cu117.html`

#### Build LightGBM for GPU
https://stackoverflow.com/questions/60360750/lightgbm-classifier-with-gpu

Please reach out to us if you have any questions! :)
