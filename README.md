# pytest_split_zero_tests
test repo to check if I can reproduce an issue with pytest split


## pytest split with 0 selected tests
To reproduce, issue these commands:
```
pytest tests --splits 3 --group 1 --verbose
pytest tests --splits 3 --group 2 --verbose
pytest tests --splits 3 --group 3 --verbose
```
You will get for the groups, in order,
```
collected 26 items / 5 deselected / 21 selected
collected 26 items / 21 deselected / 5 selected
collected 26 items / 26 deselected / 0 selected
```
