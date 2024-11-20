# Metaproteomics Analysis 

This folder contains code and files related to the DIA and PRM analysis of the 2021 time series from Orcas Island, WA, USA. 

## File Descriptions: 

HABTimeSeries_probedata.csv: File contains all metadata collected by YSI EXO1 Sonde probe, with collection points every 5-10 minutes. Columns include Date, Time, chlorophyll concentration in RFU and ug/L, (Chlorophyll.RFU, Chlorophyll.ugL), conductivity in us/cm (Conductivity.uscm), depth in meters (Depth.m), dissolved oxygen in percent saturation and mg/L (ODO.sat, ODO.mgL), salinity in psu (Sal.psu), pH, temperature in degrees Celsius (Temp.C), battery voltage of the probe (Battery.V), and a combined date and time column (Date.Time). 

HAB_2021_DDA_metagenome_contam_v1.4.10-1.12.31_TICnormalized_092722_36samples_final_Rcleaned.csv: File contains quantitative peptide abundances collected using data-independent acquisition (DIA) for the metaproteomic time series. The first column contains the peptide identification. The following columns contain the peptide abundances for each sample, with column names indicating the day of collection and the hour of collection separated by a period. For example, column 16.17 was collected on day 17 at hour 17:00. Columns are in order of collection, with samples collected every 4 hours. 

HAB_2021_Nuts_metadata.csv: File contains metadata for every metaproteomic sample collection point, including every four hours (01:00, 05:00, 09:00, 13:00, 17:00, 21:00). Columns include Date, Time, and a combined date and time column (DateTime). Averaged cell counts from triplicate measures of cyanobacteria, picoeukaryotes (Picoeuks), and nanoeukaryotes (Nanoeuks) are reported in cells/mL from flow cytometry analysis. Light intensity (Intensity....lum.ft2.) and metadata from YSI EXO1 Sonde Probe are reported as in the file HABTimeSeries_probedata.csv (Chlorophyll.RFU, Conductivity.uscm, ODO.sat, Sal.psu, pH, Temp.C). Nutrient concentrations are reported in units mM for phosphate (PO4), silicate (Si.OH.4), nitrate (NO3), nitrite (NO2), and ammonium (NH4). 

HAB_2021_WGCNA_datTraits_corr1.csv: File contains columns with sample, date, and day to run code for PCA. 

HAB_2021_probe_timeseries_binned.csv: File contains metadata collected by YSI EXO1 Sonde probe for every sample analyzed by mass spectrometry in the Discovery analysis. Columns include combined date and time (Date.hour), chlorophyll concentration (Chlorophyll.ugL), temperature in degrees Celsius (Temp.C), conductivity in us/cm (Conductivity.uscm), salinity in psu (Sal.psu), pH, and percent saturation of dissolved oxygen (ODO.sat). Binning involved averaging values collected every 5-10 minutes to create an average measure for each hour. 

HAB_2021_taxa_counts_annotations_all.csv: File contains annotations and data from MetaGOmics analysis for all metaproteomic samples in the Discovery data set. Columns include Gene Ontology (GO) accession number (GOacc), GO aspect (GOtype), GO term name (GOterm), taxonomy rank (taxonrank), taxonomy name (taxon), NCBI taxonomy id, and quantitative peptide abundances for each sample with numbers denoting day of collection and time of collection separated by a period and prefaced by “PSMcount_”. A total of 36 time points are included in the Discovery analysis. 

HAB_flowcytometry.xlsx: Excel file contains two tabs (Phytoplankton, Bacteria) with cell counts in cells per milliliter resulting from the flow cytometry analysis. Phytoplankton measures were collected in triplicate and bacterial measures were collected in duplicate. Columns include Day, Hour, Sample ID, and Date in each tab. The Bacteria tab contains one measure for the bacterial microbiome. The Phytoplankton tab contains measures for cyanobacteria, picoeukaryotes (Picoeuks), and nanoeukaryotes (nanoeuks) as separated by size fraction. 

HAB_metadata_MARSS.csv: File contains metadata for each sample analyzed by metaproteomics in the Discovery analysis. Columns include Date, hour (Time), combined date and time (DateTime), light intensity (Intensity....lum.ft2.), nutrient concentrations for phosphate (PO4), silicate (Si.OH.4), nitrate (NO3), nitrite (NO2), ammonium (NH4), chlorophyll concentration in micrograms per liter (chl), temperature in degrees Celcius (temp), percent saturation of dissolved oxygen (O2), cell counts in cells per milliliter of cyanobacteria (cyano), picoeukaryotes (pico), and nanoeukaryotes (nano), and a combined date and time column (Date.Time). 


Orcas-Island-Time-Series-Metaproteomics.Rmd
File contains all code for running statistical analyses and creating figures.
