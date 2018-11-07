Some info that might be helpful for us.

## Version control

* `git pull/push origin master` to push to and pull from our own Github repo
* To grab updates from the competition board, do:
    1. `git remote add og https://github.com/TRANSFORABJ70/TRANSFOR19.git` to add a reference to the official repo (only need to do this once)
    2. `git pull og master` to actually grab the changes and merge them into our repo

Generally we want to avoid changing any files that the official repo controls (e.g. `area.png`, `Predictions.zip`, and `README.md`).

## Dataset

Original datafile's too big to commit so [here it is](https://drive.google.com/file/d/1ViX3FxWIN-L4Umx9svy-P_gMflsqgOa5/view?usp=sharing). Drop it into the main directory and git will be preset to ignore it.

From the board's email introducing the data:
>In Github, we have posted the Predictions file containing 2 csv files (North and South direction). Predictions should be generated for the time periods 6:00 to 11:00 and 16:00 to 21:00 (marked with “x”).
>You can also find the entire city trajectories for the same day (gps_20161201) here.

## Projecting

If we use map information, make sure to use the [eviltransform library](https://github.com/googollee/eviltransform) to convert back and forth between standard projection coordinates (WGS-84) and the Chinese-specific projection coordinate system (GCJ-02).
