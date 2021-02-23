![image](https://github.com/patternizer/rbeast-frontend/blob/master/glosat-gmted-haversine.png)

# glosat-gmted-haversine

[GloSAT](https://www.glosat.org) outlier detection python code that uses the Haversine distance to locate 3x3 cells in a hi-res (0.0625 degree) QGIS extract of GMTED2010 centered on monitoring stations and then evaluates differences in expected latitude, longtidue and elevation as an error probe. 

* python code to perform the outlier detection calculations
* plots GloSAT station elevations
* plots GloSAT station Delaunay interpolation
* plots GloSAT station Haversine distance check from (0,0)
* plots GloSAT-GMTED2010 elevation differences [3x3 station-centered]
* plots GloSAT-GMTED2010 latitude differences [3x3 station-centered]
* plots GloSAT-GMTED2010 longitude differences [3x3 station-centered]
* plots GMTED2010 elevation interpolated contour map

## Contents

* `glosat-gmted-haversine.py` - python outlier detection code
* `gmted2010_15n015_00625deg-hi-res.png` - GMTED2010 elevation interpolated contour map

The first step is to clone the latest glosat-gmted-haversine code and step into the check out directory: 

    $ git clone https://github.com/patternizer/glosat-gmted-haversine.git
    $ cd glosat-gmted-haversine

### Using Standard Python

The code should run with the [standard CPython](https://www.python.org/downloads/) installation and was tested 
in a conda virtual environment running a 64-bit version of Python 3.6+.

glosat-gmted-haversine scripts can be run from sources directly, once the data dependencies are resolved:

* `GMTED2010_15n015_00625deg.nc` - GMTED2010 QGIS extracted hi-res (0.0625 degree) global elevation data in netCDF-4 format
* `df_temp.pkl` - python dataframe of GloSAT.p01 data in .pkl format
* `df_nearest.pkl` - python dataframe of Haversine distances to GMTED2010 cells in .pkl format

Data is available from [Michael Taylor](michael.a.taylor@uea.ac.uk).

Run with:

    $ python glosat-gmted-haversine

## License

The code is distributed under terms and conditions of the [Open Government License](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).

## Contact information

* [Michael Taylor](michael.a.taylor@uea.ac.uk)

