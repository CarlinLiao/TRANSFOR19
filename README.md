# Intro

This is the neural network model we at SPARTA built to infer vehicle speed on a certain link in the Xi'an road network given Didi data in the local area (sans that link) as per the TRANSFOR19 competition. [See full competition details and results here](https://github.com/TRANSFORABJ70/TRANSFOR19) and refer to both the Jupyter notebooks and `SPARTA_transfor.pdf` for further details on our model.

# Notes for SPARTA research group members

Some info and details that might be helpful for us.

## Version control

* `git pull/push origin master` to push to and pull from our own Github repo
* To grab updates from the competition board, do:
    1. `git remote add og https://github.com/TRANSFORABJ70/TRANSFOR19.git` to add a reference to the official repo (only need to do this once)
    2. `git pull og master` to actually grab the changes and merge them into our repo

Generally we want to avoid changing any files that the official repo controls (e.g. `area.png`, `Predictions.zip`, and `README.md`).

## Dataset

The original datafile for December 1, 2016 whose average speeds we were asked to predict is too big to commit so [here it is](https://drive.google.com/file/d/1ViX3FxWIN-L4Umx9svy-P_gMflsqgOa5/view?usp=sharing). Drop it into the main directory and git will be preset to ignore it.

From the board's email introducing the data:
>In Github, we have posted the Predictions file containing 2 csv files (North and South direction). Predictions should be generated for the time periods 6:00 to 11:00 and 16:00 to 21:00 (marked with “x”).
>You can also find the entire city trajectories for the same day (gps_20161201) here.

We can request the full dataset for October and November from the Didi's [Gaia Initiative](https://outreach.didichuxing.com/research/opendata/en/) webpage. These raw files go in `data/tar/` and will be unzipped to `/data/xian` by `2a_data_download.ipynb`.

## Projecting

If we use map information, make sure to use the [eviltransform library](https://github.com/googollee/eviltransform) to convert back and forth between standard projection coordinates (WGS-84) and the Chinese-specific projection coordinate system (GCJ-02).
