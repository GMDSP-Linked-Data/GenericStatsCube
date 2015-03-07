Generic Stats
=================

Overview
--------
A generic Refine project to model statistics as RDF data cubes.


Use case
--------
This could be applied to datasets that detail counts/aggregates against multiple parameters (eg: place & time).


Ontologies
----------
This work utilises the RDF Data Cube Vocabulary: http://www.w3.org/TR/vocab-data-cube/.


Contents
--------
The package consists of:

- Example spreadsheet
- Example Open Refine project
- JSON files to use in the Refine model
- Example output RDF file

Installation
----------------
To replicate the example RDF file, follow these steps:

1 - Download/Open/Run Open Refine (http://openrefine.org/)
1a - Add the RDF Extension to Refine (http://refine.deri.ie/) 
2 - "Create Project" in Refine, using the "ExampleStatsCube-data.csv" file.
3 - Once open, use the Apply/Extract function to run the following steps (copy and paste the JSON):
-- Step 1 - Create an ID for each observation - use file "1-genericStats-ID.json" 
-- Step 2 - Reconcile areas* - use file "2-genericStats-ReconcileAreas.json" (this step can be skipped if areas are not applied).
-- Step 3 - Apply the RDF Skeleton - use file "3-genericStats-RDF-Skeleton.json"
4 - Once completed output the RDF file via Export > RDF (as either XML or Turtle)

Or

Open Refine > Import Project > "ExampleStatsCube-RefineProject.google-refine.tar.gz" will get you to the step 3!

*NB: This model reconciles against the Ordnance Survey and ward areas.

Using the model
-------------------
This model can be used and adapted for a variety of uses.  The 3-genericStats-RDF-Skeleton.json file can be applied to other files in Open Refine, provided that column headings are the same.  Follow these tips when doing so:

- Utilise the same column headings as "ExampleStatsCube-data.csv"
- When applying the RDF Skeleton, it is possible to just edit:

>       "baseUri": "http://data.gmdsp.org.uk/data/example/stats/",

- it is possible to Find & Replace this URL with a different Base URI - this will update the rest of the JSON, which can be applied to a dataset
- Take care with the labels used in this example file - rename them accordingly

What's Missing?
-------------------
This model does not use the concept of Slices within the data cube

Status: ready for use 
---------------------
Last update: 7th March 2015


