# ext_MC_2026
Files applicable to the paper "Optical-Infrared Extinction Variation in Nearby Molecular Clouds." This repo consists of the catalog output from the paper and some samples of how to use the data.

This file contains E(B-V) and R(V) values for APOGEE targets from SDSS  DR17 using the methods outlined in Hobson-Ritz et al (2026). These values are prior to the transformation into the Zhang et al (2025) scaling. To convert the R(V) values to that scaling, multiply the rv column by 0.974 and subtract 0.197. The 1 sigma errors for R(V) are the R(V) 1 sigma error due to photometric errors taken in quadrature with 0.1.

The catalog contains the following fields: 

l: Galactic longitude of star
b: Galactic latitude of star
mag: PS1(g,r,i,z,y), 2MASS(J,H,K), & WISE(W1,W2) mag
mag_err: Uncertainties in mag
mag_int: Estimated intrinsic magnitudes of star from APOGEE stellar parameters and Hobson-Ritz et al. (2026), corresponding to mag. An overall constant or gray term is undetermined.
ebv: E(B-V) to star
ebv_err: Uncertainties in ebv
rv: R(V) to star
rv_err: Uncertainties in rv
x: Extinction curve parameter x to star
p: Parallax of star from Gaia early data release 3
p_err: Uncertainties in p
flags: Bit mask of flags, see description below
cloud_ID: ID for molecular clouds, see below
T: Planck dust equilibrium temperature to star
T_err: Uncertainties in T
beta: Planck dust emission spectral index to star
beta_err: Uncertainties in beta
tau: Planck optical depth at 353GHz to star
tau_err: Uncertainties in tau
radiance: Planck integrated emission to star

Cloud IDs:

0: Not used in MC analysis
1: Taurus
2: Perseus
3: Orion A
4: Orion B
5: Monoceros
6: NGC 2264
7: Ophiuchus
8: California
9: NGC 1579
10: Rosette

Flags:

0: ebv < 0.3, rv will be particularly uncertainty
1: photometry with uncertainty < 0.2 available in < 7 bands; use with caution
2: photometry with uncertainty < 0.2 available in < 9 bands
3: uncertainty in g, r, or W2 photometry > 0.2, rv will be unreliable
4: significant uncertainty in rv, use with caution
