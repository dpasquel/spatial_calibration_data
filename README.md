This repository is an add-on of: Pasquel, D., Taylor, J.A., Tisseyre, B. and Roux, S.  *About drivers of performance for crop growth model calibration at the within-field scale*. Submitted to *European Journal of Agronomy*. 2025

It contains the simulated and observed values of vineyard predawn water potential used in the paper to analyze the performance of a spatial calibration procedure. Details on simulated and experimental data can be found in the associated article.

## Repository Contents

- `data/`
  - `obs.sim_field.scale.Rdata`: PWS observed and PWS simulated at the field scale for each measurement site for each measurement date.
  - `obs.sim_Z2.scale_corr10.Rdata`: PWS observed and PWS simulated at 2-zone within-field scale delineated with ancillary data at 10% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z2.scale_corr50.Rdata`: PWS observed and PWS simulated at 2-zone within-field scale delineated with ancillary data at 50% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z2.scale_corr90.Rdata`: PWS observed and PWS simulated at 2-zone within-field scale delineated with ancillary data at 90% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z3.scale_corr10.Rdata`: PWS observed and PWS simulated at 3-zone within-field scale delineated with ancillary data at 10% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z3.scale_corr50.Rdata`: PWS observed and PWS simulated at 3-zone within-field scale delineated with ancillary data at 50% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z3.scale_corr90.Rdata`: PWS observed and PWS simulated at 3-zone within-field scale delineated with ancillary data at 90% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z4.scale_corr10.Rdata`: PWS observed and PWS simulated at 4-zone within-field scale delineated with ancillary data at 10% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z4.scale_corr50.Rdata`: PWS observed and PWS simulated at 4-zone within-field scale delineated with ancillary data at 50% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z4.scale_corr90.Rdata`: PWS observed and PWS simulated at 4-zone within-field scale delineated with ancillary data at 90% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z5.scale_corr10.Rdata`: PWS observed and PWS simulated at 5-zone within-field scale delineated with ancillary data at 10% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z5.scale_corr50.Rdata`: PWS observed and PWS simulated at 5-zone within-field scale delineated with ancillary data at 50% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_Z5.scale_corr90.Rdata`: PWS observed and PWS simulated at 5-zone within-field scale delineated with ancillary data at 90% of correlation with the observed PWS for each measurement site for each measurement date.
  - `obs.sim_site.scale.Rdata`: PWS observed and PWS simulated at the measurement site scale for each measurement site for each measurement date.


## File Descriptions

Each .Rdata file corresponds to a list object. For each .Rdata file, the first levels of the list correspond to the spatial structure modalities (3 different levels : strong, moderate and weak) ; the second levels of the list correspond to the 40 fields of each spatial structure modalities. Each field is represented by a data.frame with the 49 sites of measurement for each measurement dates (not only the considered in the article).

In the studies, 1080 simulations were considered corresponding to :
40 fields * 3 spatial structure modalities * 3 levels of correlation with the ancillary data * 3 spatial calibration level considered (i.e. field, site scale + the best within-field segmentation)

Note that, the .Rdata contain all  segmentations realized for the study (not only the best one).

For each data.frame, the file structure is as follow :

| Column             | Description                                                                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Date`             | Date (YYYY-MM-DD)                                                                                                                                                       |
| `E`                | Eastern point reference                                                                                                                                                 |
| `N`                | Northern point reference                                                                                                                                                |
| `measurement_site` | Number of the site within vineyard                                                                                                                                      |
| `PWS_obs`          | Vine water potential observed                                                                                                                                           |
| `PWS_sim`          | Vine water potential simulated (at the considered spatial scale)                                                                                                        |
| `cz.X.YYY`         | For the within-field modalities, this is the zone to which belongs the considered measurement site (X : level of segmentation ; YYY : level of correlation with the AD) |


## Contact

If you have any question, please contact :  
*Daniel PASQUEL* – daniel.pasquel@inrae.fr

## Author

Daniel Pasquel, INRAE, 2025
