# FOCAL_OpenFast_C4
OpenFAST model from the National Renewable Energy Laboratories / University of Maine Floating Offshore-wind Controls Advanced Laboratory Experimental Campaign 4

This model can be used with the OpenFAST executable found [here](https://drive.google.com/drive/folders/1mzSc-gbeguHG0a25sF_BfvjU3HSYAXpr?usp=sharing).

Notes about the OpenFAST model:
1. Due to sensor limitations, the wind calibration time history from the experiment files will not result in proper performance of the OpenFAST model.
   Instead, use the files provided in the "Wind" subfolder.
   The data in these files is derived from post-campaign wind calibration studies such that both mean wind speed and turbulence are represented correctly.

2. OpenFAST doesn't allow to include the tower eccentricity (x = 3.31 m and y = 0.49 m) -> The tower has the proper mass and the eccentricity has been introduced in the platform CM.

3. The platform mass and inertia has been reduced because the TMDs (even when they are locked) are included separately.
   The platform properties without TMDs are:
    m = 1.660E7 kg
    CMx = 0.09 m
    CMy = -0.6745 m
    CMz= -13.7 m from mean sea level
    Ixx @ CM = 1.112E10 kgm^2
    Iyy @ CM = 1.248E10 kgm^2
    Izz @ CM = 9.706E9 kgm^2

4. Platform mass offsets when including the x and y tower mass eccentricity:
    CMx = 0.22 m
    CMy = -0.656 m  
