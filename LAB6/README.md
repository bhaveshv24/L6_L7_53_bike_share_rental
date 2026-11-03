# L6_L7_53 — Bike Share Rental

Lab 6: Code and Branch Coverage

## About

A small Python module that prices bike-share rides by bike type, duration and subscription, reports dock status and decides whether a rider may unlock a bike.

## Files

| File | Description |
|------|-------------|
| `bike_share_rental.py` | The module under test |
| `CodeCoverageTest_53_bike_share_rental.py` | 17 statement coverage cases |
| `BranchCoverageTest_53_bike_share_rental.py` | Retains 17 cases and adds 40 decision/boundary cases |
| `test_bike_share_rental.py` | Default pytest collection entry point |
| `run_coverage.py` | Reproducible runs, saved output, JSON and HTML reports |
| `evidence/line_coverage.png` | Screenshot of the final line coverage output |
| `evidence/branch_coverage.png` | Screenshot of the final branch coverage output |
| `evidence/coverage_html_summary.png` | Generated HTML report screenshot |
| `evidence/coverage_functions.png` | Generated per-function report screenshot |

## Run the line coverage stage

From the repository root, create and activate a Python 3 virtual environment,
then install `LAB6/requirements.txt`. Run:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r LAB6/requirements.txt
python LAB6/run_coverage.py line
python LAB6/run_coverage.py branch
python -m pytest -q
```

The stage measures only `bike_share_rental.py`, not the tests. It passes 17
cases and covers all 40 executable statements (100%). Saved baseline logs in
`evidence/baseline/` record the original two tests and their 50% line coverage.

The final branch stage passes 57 cases: 40/40 statements and 30/30 branch
outcomes, both 100%, with no partial branches. The original branch run covered
11/30 branch outcomes (36.67%); its terminal `Cover` column is the combined
statement/branch score, 44%, rather than the standalone branch percentage.

The branch test module imports the line tests so that either named deliverable
can be run independently. The default `test_bike_share_rental.py` imports the
complete suite, allowing ordinary pytest discovery without duplicate cases.
Explicitly collect one entry point per run. All expectations are asserted;
the application source is unchanged and nothing is excluded from coverage.

The PNG evidence captures a local browser view of saved, verbatim command
output and the actual generated coverage HTML. Full transcripts and JSON data
are retained alongside the images. The `COVERAGE_FILE` variable is set by the
runner to preserve independent line/branch data; use the runner to reproduce.

Coverage measures execution, not proof of correctness or exhaustive path/
condition coverage. Extra cases cover short-circuit inputs and returned
boolean thresholds that line-based branch measurement alone may not count.

Keep all your Lab 6 work in this `LAB6` folder. Lab 7 will be added to this repo later.

Refer to the lab handout for instructions.
