# Healthcare Survey Project

This project implements a survey tool for collecting and analyzing income spending data for a healthcare product launch.

## Setup Instructions

1. **Environment Setup**:
   - Install Python 3.10+ and packages: `pip install flask pymongo pandas matplotlib seaborn jupyter`.
   - Set up MongoDB Atlas and export `MONGO_URI` environment variable.

2. **Run Flask App**:
   - `python app.py`
   - Access at http://127.0.0.1:5000/ to submit data.

3. **Export to CSV**:
   - `python export_to_csv.py`

4. **Analysis**:
   - Open `analysis.ipynb` in Jupyter: `jupyter notebook`
   - Run all cells to generate visualizations and exports.

5. **AWS Deployment**:
   - Launch EC2 instance (Ubuntu).
   - SSH in, install deps, copy files, set MONGO_URI.
   - Run with Gunicorn: `gunicorn -w 4 -b 0.0.0.0:8000 app:app`
   - Update security group for port 8000.

## Notes
- Test with sample submissions.
- Visualizations are exported as PNG for PowerPoint.
- For R alternative: Use `data.table` for processing, `ggplot2` for viz (not implemented here).
