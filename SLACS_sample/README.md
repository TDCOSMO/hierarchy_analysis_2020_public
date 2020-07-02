# SLACS sample
This repository hosts the individual lens posteriors and kinematic data of the SLACS sample.


## Tables
The table slacs_all_params.csv consists of the information on the SLACS sample and the imaging modeling posteriors from Shajib et al. 2020.

The table LineOfSightData.csv contains the galaxy number count and local overdensity statistics of the SLACS sample.
Of relevance are 'Nmed' (median number count within the 2 arcmin aperture). 'NoverRmed' 1/r weighted number count in same aperture and the random field averages of those quantities.

SLACS_V_disp: Updated velocity dispersion measurements from SDSS by Adam Bolton
vdisp_slacs_asb.fits: equivalent to SLACS_V_disp in fits format.


## Folders
The table SLACS_V_vdisp.csv consists of different reductions of the SDSS spectra velocity dispersion measurements.

The folder IFU_data consists of the VLT-VIMOS IFU data products from Czoske et al. 2008.

The folder kappaSLACS contains all the external convergence probability distributions for the individual lenses from the relative weighted number counts.


## Jupyter Notebooks

The jupyter notebook IFU_SLACS_display.ipynb displays all the 2d kinematic maps and the azimuthal bins chosen in this analysis.

The jupyter notebook kinematic_sample_slacs_preprocessing.ipynb processes the indificual constraint and combineds imaging and spectroscopic constraints in a common format for IFU and SDSS spectra.

The jupyter notebook SLACS_constraints.ipynb performs the hierarchical analysis of the SLACS sample.



The labels in the table slacs_all_params.csv which are relevant:
- name: string, name of lensing system as coordinates
- flag_imaging: integer, indicating the quality of the lens modeling based on imaging data. 1 is good quality, 0 is some issues remaining, -1 useless
- flag_los: integer, 1 means no major perturber nearby impacting the lensing, 0 means issues with LOS, -1 is major impact
- IFU: 1 if IFU data is available, 0 if not
- theta_E: Einstein radius of the main deflector in units of arc seconds (from Shajib et al. 2020)
- theta_E_error: 1-sigma uncertainty in the Einstein radius (from Shajib et al. 2020)
- gamma: power-law slope of the PEMD model based on imaging data only (from Shajib et al. 2020)
- gamma_error: 1-sigma uncertainty in the power-law slope (from Shajib et al. 2020)
- z_lens: redshift of the lens
- z_source: soruce redshift
- sigma_v: SDSS velocity dispersion measurement of main deflector (Bolton et al. 2008) (we are using updated values from a fits file)
- sigma_v_error: 1-sigma error in the velocity dispersion measurement (Bolton et al. 2008) (we are using updated values from a fits file)
- q: axis ratio of light in main deflector (minor/major)
- r_eff: projected half-light radius of the deflector (HST V-band, Auger et al. 2009)
- r_eff_error: 1-sigma error in r_eff
- comment_imaging: comments/issues in the imaging analysis
- n_bin: integer, number of radial bins for the IFU data binning
- r_max: maximal radius (arc seconds) of the IFU data binning
- psf_ifu: FWHM (arc seconds) of the PSF in the IFU observation
- fiber_scale: separation of fibers in the VIMOS data
- flag_ifu: integer, flag whether IFU data is useful for anisotropy constraints (e.g. no unusual rotation, perturber etc)
- ifu_file_name: file name of the fits file containing the IFU maps for the lens
- comment_ifu: comments on the IFU data
- RA: RA (J2000)
- DEC: DEC (J2000)

