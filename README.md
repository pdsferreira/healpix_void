# healpix_void
Healpix mod code to apply voids on healpix maps (during spherical harmonics mapping) using the expected lensing angle function. Extension of the [Healpix boost](https://github.com/mquartin/healpix-boost) code.

# Instructions

Compile the fortran code, the mod was only applied in the fortran90 code. The void is applied by the synfast function. You should provide the polynomial coefficients of the lensing angle function in terms of theta/thetaL, where thetaL is the angular size of the void and theta is the colatitude (e.g. a + b*theta/thetaL + c*(theta/thetaL)^2 + d* (theta/thetaL)^3, a,b,c and d are the polynomial coefficients). The void is applied in the north pole, but can be rotated using the modified alteralm function (see [Healpix boost](https://github.com/mquartin/healpix-boost)).

# Warning

Do not apply aberration and Doppler effects combined with the void in this version, this was not tested yet.

# Dependencies
* fortran 90 (main boost code)
* Healpix
* [Healpix boost](https://github.com/mquartin/healpix-boost)
