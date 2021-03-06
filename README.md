# rainfall-teleconnections
Python code to compute global teleconnections from rainfall data

## Author
Niklas Boers

## License
This work is licensed under the GNU General Public License v3.0. For details please read LICENSE.txt.

## General notes
This repository hosts python code to compute network representations of synchronizations between extreme rainfall events at different locations on the globe. The analysis is based on the Tropical Rainfall Measurement Mission (TRMM) 3B42 V7 dataset, which is available for download at https://pmm.nasa.gov/data-access/downloads/trmm.

## Requirements
numpy scipy weave scikit-learn netCDF4 windspharm matplotlib basemap

## Usage
The scripts should be run in the following order:

#### 1. events_from_data.py
loads the data and computed events above predefined percentile thresholds

#### 2. events_plots.py
plots the values of the percentile thresholds, and the corresponding numbers of events at each location

#### 3. Event_Synchronization_null_model.py
computes the null model distribution for the Event Synchronization (ES) measure, based on surrogates with different event rates

#### 4. Event_Synchronization.py
computes the ES measure in parallel, and saves the slices as binary arrays, with an entry equal to one if the corresponding ES value is above the significance threshold, chose at the 99.5th percentile of the null model distribution.

#### 5. network_construction.py
computes the networks and corresponding geographical link distances.

#### 6. distance_distribution.py
computes the distance distribution as a histogram of all link distances

#### 7. distance_distribution_plot.py
plots the distance distribution together with a corresponding power law fit

#### 8. distance_distribution_percentile_dependence.py
compares the distance distributions for different event strengths

#### 9. distance_distribution_tropical_vs_extratropical.py
compares the distance distributions for different spatial subsets such as the tropics or the extratropics of both hemispheres

#### 10. link_bundles.py
determines the links associated with the study region in South-Central Asia, and estimates their spatial density using a Kernel Density Estimator

#### 11. link_bundles_null_model.py
computes the null model of the spatial density of links associated with South-Central Asia

#### 12. link_bundles_plots.py
plots the link bundles and the corresponding null model distribution

#### 13. sync_times_between_regions.py
determines times of high extreme event synchronizations between Europe and South-Central Asia

#### 14. v_gph_psi_anomalies.py
computes composite anomalies of meridional wind speeds, geopotential height, and streamfunction for times of high extreme event synchronizations between Europe and South-Central Asia

#### 15. v_gph_psi_anomalies_plots.py
plots the composite anomalies of meridional wind speeds, geopotential height, and streamfunction

