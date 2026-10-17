# Python Data Quality Checker

Command-line CSV profiler for blank values, duplicate rows, duplicate identifiers, and simple email-format anomalies.

## Quick start
Python 3.10+ and pandas required.
```bash
python -m pip install -r requirements.txt
python src/data_quality_check.py data/sample_customers.csv --id-column customer_id --email-column email
python -m unittest discover -s tests -v
```

The sample data intentionally includes quality issues. The tool reports issues but does not modify the source file. Email screening is a heuristic, not proof of deliverability; duplicate IDs require context-specific review.
