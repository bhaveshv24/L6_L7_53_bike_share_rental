# L6_L7_53 — Bike Share Rental

Lab 6: Code and Branch Coverage

## About

A small Python module that prices bike-share rides by bike type, duration and subscription, reports dock status and decides whether a rider may unlock a bike.

## Files

| File | Description |
|------|-------------|
| `bike_share_rental.py` | The module under test |
| `CodeCoverageTest_53_bike_share_rental.py` | 17 statement coverage cases |
| `test_bike_share_rental.py` | Default pytest collection entry point |
| `run_coverage.py` | Reproducible runs, saved output, JSON and HTML reports |
| `evidence/line_coverage.png` | Screenshot of the final line coverage output |

## Run the line coverage stage

From the repository root, create and activate a Python 3 virtual environment,
then install `LAB6/requirements.txt`. Run:

```bash
python LAB6/run_coverage.py line
```

The stage measures only `bike_share_rental.py`, not the tests. It passes 17
cases and covers all 40 executable statements (100%). Saved baseline logs in
`evidence/baseline/` record the original two tests and their 50% line coverage.

Keep all your Lab 6 work in this `LAB6` folder. Lab 7 will be added to this repo later.

Refer to the lab handout for instructions.
