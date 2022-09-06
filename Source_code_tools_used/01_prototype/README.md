# Prototype: Adaptive Swarm
This is for QE.

## Quick start
```bash
$ python src/planner.py adswarm -k vanilla -rs <seed rand num start> -re <seed rand num end>
```

## Result
Result files are stored in `output` folder.
`contribution.log` has DCC's raw delta data.


## Experiment configuration
Change below code in conf.py,

```python
'''
Environment configuration
'''
MAP_SIZE = 1000  # original is 500
MAP_BOUNDS_METER = 5.0  # original is 2.5

MAP_SIZE_new_x = 400#2000
MAP_SIZE_new_y = 2000#400
MAP_BOUNDS_METER_new_x = 2.0#10.0
MAP_BOUNDS_METER_new_y = 10.0#2.0

# for backup TODO: remove this after a while

# XY_START = np.array([-9.0, 0.7]) 
# XY_GOAL = np.array([9.0, 1.0])

XY_START = np.array([1.2, 9.0]) # for vertical map
XY_GOAL = np.array([-1.0, -6.0]) # for vertical map

```
- Obstacle: `obstacle.py`.

## Clean-up and store the output data

```
./output_store.sh <name of data folder>
```
It will make a folder and move all files in `output` folder to it.

```
./output_cleanup
```
It will move all files in `output` folder to `data/deprecated`.
