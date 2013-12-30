About
=====

Scripts to calculate moment diagnostics for the stratospheric polar vortex. These
can be used, for instance, to diagnose split and displaced vortex events, as
described in [_Seviour et al., 2013_](http://onlinelibrary.wiley.com/doi/10.1002/grl.50927/abstract).

* This repository contains two main scripts **vor.py** (a Python script) 
and **vor.pro** (an IDL script). Both are able to calculate moment diagnostics.
* Required packages are ``numpy`` and ``scipy.interpolate``.
* Example uses:

**vor.py:**
```python
import vor
d = vor.calc_moments(field,lats,lons,'NH','GPH',29600) 
```
**vor.pro:**
``` IDL
d=VOR(field,lon,lat,/GP,EDGE=3.02e4)
```
* For a full example of using vor.py, please see **moments_1979_example**. Note this may take about 10 minutes to run on a normal PC. 

Citations
=========
If you use the Python script **vor.py** please cite: 

Seviour, W. J. M., D. M. Mitchell, and L. J. Gray (2013), A practical method to identify displaced and split stratospheric polar vortex events, _Geophys. Res. Lett._, 40, 5268-5273 [doi:10.1002/grl.50927](http://onlinelibrary.wiley.com/doi/10.1002/grl.50927/abstract)

If you use the IDL script **vor.pro** please cite:

Mitchell, D.M., Charlton-Perez, A.J. and Gray, L.J. Characterising 
the Variability and Extremes of the Stratospheric Polar Vortices 
Using 2D Moments, _J.Atmos.Sci._, 1194-1213, 2011. [doi:10.1175/2010JAS3555.1](http://journals.ametsoc.org/doi/abs/10.1175/2010JAS3555.1)

