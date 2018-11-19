# Massachusetts Election Shapefiles
These shapefiles were compiled by Metric Geometry and Gerrymandering Group (MGGG) staff, Radcliffe Research Partners, and members of the Voting Rights Data Institute. The Voting Rights Data Institute (VRDI) was a 2018 summer intensive sponsored by the Metric Geometry and Gerrymandering Group (MGGG) at Tufts and MIT, with major support from a Bose Research Grant at MIT and from the Jonathon M. Tisch College of Civic Life at Tufts.

## Sources
The 2012-2016 raw, unprocessed precinct shapefile comes from the office of the Secretary of the Commonwealth of Massachuestts, William Francis Galvin. The 2002-2010 raw, unprocessed shapefile comes from the United States Census Bureau (available for download here: https://catalog.data.gov/dataset/tiger-line-shapefile-2012-2010-state-massachusetts-2010-census-voting-district-state-based-vtd) and was sent to MGGG from Secretary Galvin's office. All election data comes from the Secretary of the Commonwealth's Elections Division website (available here http://electionstats.state.ma.us).

## Processing
In order to join election data to the precinct shapefiles, certain pre-processing steps were taken. Certain precincts in the election results csv were aggregated into one precinct to match the shapefile. For example, in the 2012-2016 elections votes in Andover precinct 7 and 7A were aggregated into one precinct, Andover precinct 7. In the 2002-2010 shapefile, Ware precinct 2 and precinct 3 were merged into one precinct. Undefined areas in the 2002-2010 shapefile (meaning areas encompassing only water with zero population) were deleted. A script was used to create unique identifiers for the election results csvs in order to join them to the shapefiles. The script faster_proration_with_counties.py (available in https://github.com/gerrymandr/Preprocessing) was used to aggregate 2000 Census population from census blocks to 2002-2010 precincts.

## Metadata
Below is a brief description of each of the listed variables in the attribute table of the 2002-2010 shapefile:
- `STATEFP10`: State FIPS code
- `COUNTYFP10`: County FIPS code
- `VTDST10`: Voting tabulation district FIPS code
- `GEOID10`: 8-digit FIPS code
- `VTDI10`: 2010 Census voting district indicator
- `NAME10`: Voting tabulation district name
- `NAMELSAD10`: Translated statistical area description code
- `LSAD10`: 2010 Census legal/statistical area description code for voting district 
- `MTFCC10`: MAF/TIGER feature class code
- `FUNCSTAT10`: 2010 Census functional status
- `ALAND10`: Area land (square meters)
- `AWATER10`: Area water (square meters)
- `INTPTLAT10`: Latitude of internal point
- `INTPTLONG10`: Longitude of internal point
- `City/Town`: Municipality name
- `Ward`: Ward number/letter
- `Pct`: Precinct number/letter
- `SEN02D`: Number of votes for 2002 Democratic senate candidate
- `SEN02R`: Number of votes for 2002 Republican senate candidate
- `PRES04D`: Number of votes for 2004 Democratic presidential candidate
- `PRES04R`: Number of votes for 2004 Republican presidential candidate
- `SEN06D`: Number of votes for 2006 Democratic senate candidate
- `SEN06R`: Number of votes for 2006 Republican senate candidate
- `PRES08D`: Number of votes for 2008 Democratic presidential candidate
- `PRES08R`: Number of votes for 2008 Republican presidential candidate
- `SEN08D`: Number of votes for 2008 Democratic senate candidate
- `SEN08R`: Number of votes for 2008 Republican senate candidate
- `SEN10R`: Number of votes for 2010 Republican senate candidate
- `SEN10D`: Number of votes for 2010 Democratic senate candidate
- `POP2000`: Population from 2000 Census

Below is a brief description of each of the listed variables in the attribute table of the 2012-2016 shapefile:
- `District`: Ward number/letter and precinct number/letter
- `Name`: Precinct name
- `Population`: Total population from 2010 census
- `White`: White population from 2010 census
- `Black`: Black/African American population from the 2010 census
- `AmIndian`: American Indian and Alaska Native population from the 2010 census
- `Asian`: Asian population from the 2010 census
- `Hawaiian`: Native Hawaiian and other Pacific Islander population from the 2010 census
- `Other`: Population of other race from 2010 census
- `_1_Race`: Population of one race from 2010 census
- `_2__Races`: Population of two or more races from 2010 census
- `Hispanic_O`: Population of Hispanic origin from 2010 census
- `Not_Hispan`: Population not of Hispanic origin from 2010 census
- `Shape_Le_1`: Length of feature
- `Shape_Area`: Area of feature 
- `City/Town`: Municipality name
- `Ward`: Ward number/letter, where applicable
- `Pct`: Precinct number/letter
- `SEN12D`: Number of votes for 2012 Democratic senate candidate
- `SEN12R`: Number of votes for 2012 Republican senate candidate
- `PRES12D`: Number of votes for 2012 Democratic presidential candidate
- `PRES12R`: Number of votes for 2012 Republican presidential candidate
- `SEN13D`: Number of votes for 2013 Democratic senate candidate
- `SEN13R`: Number of votes for 2013 Republican senate candidate
- `SEN14D`: Number of votes for 2014 Democratic senate candidate
- `SEN14R`: Number of votes for 2014 Republican senate candidate
- `PRES16D`: Number of votes for 2016 Democratic presidential candidate
- `PRES16R`: Number of votes for 2016 Republican presidential candidate
- `POP10`: Population from 2010 census
