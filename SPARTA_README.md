Some info that might be helpful for us.

## Version control

* `git pull/push origin master` to push to and pull from our own Github repo
* To grab updates from the competition board, do:
    1. `git remote add og https://github.com/TRANSFORABJ70/TRANSFOR19.git` to add a reference to the official repo (only need to do this once)
    2. `git pull og master` to actually grab the changes and merge them into our repo

Generally we want to avoid changing any files that the official repo controls (e.g. `area.png`, `Predictions.zip`, and `README.md`).

## Projecting

If we use map information, make sure to use the [eviltransform library](https://github.com/googollee/eviltransform) to convert back and forth between standard projection coordinates (WGS-84) and the Chinese-specific projection coordinate system (GCJ-02).
