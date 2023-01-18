# ztfquery-algorithm-shepard
This the repository for the algorithm designed to update information nightly on transients specified.
The aim of this project is to use photometric catalogs to create a secondary data collection stream
of the ZTF that will detect and recognize changes in brightness below the five sigma detection level
that is normally sent to the ZTF alert stream. This will help us detect variable changes in objects
that are below the five sigma detection level but still meaningful to observe (objects changing over
longer timescales). With the approach of the start of LIGO O4, the completion of this photometric
alert stream will be integral in the function of LIGO’s new observational run.

This project was tackled using the ‘ztfquery’ and ‘astropy’ packages. They each provide a
set of useful tools that can be used to efficiently query data from IRSA (Infrared Science
Archive). The algorithm takes in a CSV file of information on all the transients we wish to
monitor. Each row in the file corresponds to an object’s field, objID (object ID), RA (right
ascension), and DEC (declination) values. Using this information, we will be able to perform a
cluster-query system based on field values and then calculate the closest match of the data using
the RA and DEC values for each object.
