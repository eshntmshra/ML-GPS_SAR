# InSAR Displacement Calibration using GPS Data

## Overview
Project for UTD's PHYS5336 course with the following objectives:
- Supervised classification of InSAR data points that are affected by noises and decorrelation, and thus needs calibration.
- Calibration of InSAR data points using supervised regression.

For the sake of the project, we make the following assumption:
- GPS data is always correct (which is not always true).

## Data

- SAR data is obtained from European Space Agency's Sentinel-1 satellites.
- The SAR data is processed using ISCE (InSAR Scientific Computing Environment) and MintPy.
- We use GPS data from EarthScope Consortium's Network of the Americas (NOTA) GNSS stations.

## Files

#### Classification.ipynb

Performs supervised classification of InSAR data points that are affected by noises and decorrelation, and thus needs calibration.

#### Regression.ipynb

Predicts calibration factor for calibration of InSAR data points using supervised regression.


## Input Data Format

The input data `(inputs-for-ml/final_ml_data.csv)` should be of the following format:

| date       | station | latitude           | longitude           | elevation        | slope            | north_gps | east_gps | vertical_gps | coherence | los_insar | bias | needs_calibration |
|------------|---------|---------------------|----------------------|------------------|------------------|-----------|----------|--------------|-----------|-----------|------|-------------------|
| YYYY-MM-DD| NAME    |   lat  |  lon | elev| slope  | $d_N$      | $d_E$      | $d_V$          |  0 - 1     | $d_{LOS}$      | 0.0  | 0/1                 |

