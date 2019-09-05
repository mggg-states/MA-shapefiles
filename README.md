# Massachusetts Election Shapefiles
These shapefiles were processed by Metric Geometry and Gerrymandering Group (MGGG) staff, Radcliffe Research Partners, and members of the Voting Rights Data Institute. The Voting Rights Data Institute (VRDI) was a 2018 summer intensive sponsored by MGGG at Tufts and MIT, with major support from a Bose Research Grant at MIT and from the Jonathon M. Tisch College of Civic Life at Tufts.

## Sources
The 2012-2016 raw, unprocessed precinct shapefile comes from the office of the Secretary of the Commonwealth of Massachuestts, William Francis Galvin. The 2002-2010 raw, unprocessed shapefile comes from the [United States Census Bureau](https://catalog.data.gov/dataset/tiger-line-shapefile-2012-2010-state-massachusetts-2010-census-voting-district-state-based-vtd) and was sent to MGGG from Secretary Galvin's office. All election data comes from the Secretary of the Commonwealth's [Elections Division](http://electionstats.state.ma.us). 2010 Decennial Census demographic data were downloaded from the [Census API](https://api.census.gov/data/2010/dec/sf1). The 2010 census block shapefile and district shapefiles for Massachusetts were downloaded from the US Census Bureau’s [TIGER/Line Shapefiles](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html). 2000 Decennial Census demographic data were downloaded from [IPUMS NHGIS](https://www.nhgis.org).

## Processing
In order to join election data to the precinct shapefiles, certain pre-processing steps were taken. Certain precincts in the election results csv were aggregated into one precinct to match the shapefile. For example, in the 2012-2016 elections votes in Andover precinct 7 and 7A were aggregated into one precinct, Andover precinct 7. In the 2002-2010 shapefile, Ware precinct 2 and precinct 3 were merged into one precinct. Undefined areas in the 2002-2010 shapefile (meaning areas encompassing only water with zero population) were deleted. Demographic data were aggregated from the census block level and precincts were assigned to districts using [MGGG's proration software](https://github.com/mggg/maup).

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
- `TOWN`: Municipality name
- `WARD`: Ward number/letter
- `PRECINCT`: Precinct number/letter
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
- `GOV02R`: Number of votes for 2002 Republican gubernatorial candidate
- `GOV02D`: Number of votes for 2002 Democratic gubernatorial candidate
- `GOV02G`: Number of votes for 2002 Green Party gubernatorial candidate
- `GOV02L`: Number of votes for 2002 Libertarian gubernatorial candidate
- `GOV02U`: Number of votes for 2002 Unenrolled gubernatorial candidate
- `GOV06D`: Number of votes for 2006 Democratic gubernatorial candidate
- `GOV06R`: Number of votes for 2006 Republican gubernatorial candidate
- `GOV06U`: Number of votes for 2006 Unenrolled gubernatorial candidate
- `GOV06G`: Number of votes for 2006 Green Party gubernatorial candidate
- `GOV10D`: Number of votes for 2010 Democratic gubernatorial candidate
- `GOV10R`: Number of votes for 2010 Republican gubernatorial candidate
- `GOV10U`: Number of votes for 2010 Unenrolled gubernatorial candidate
- `TOTPOP`: Total population in 2000 Census
- `NH_WHITE`: White, non-hispanic, population in 2000 Census
- `NH_BLACK`: Black, non-hispanic, population in 2000 Census
- `NH_AMIN`: American Indian and Alaska Native, non-hispanic, population in 2000 Census
- `NH_ASIAN`: Asian, non-hispanic, population in 2000 Census
- `NH_NHPI`: Native Hawaiian and Pacific Islander, non-hispanic, population in 2000 Census
- `NH_OTHER`: Other race, non-hispanic, population in 2000 Census
- `NH_2MORE`: Two or more races, non-hispanic, population in 2000 Census
- `HISP`: Hispanic population in 2000 Census
- `H_WHITE`: White, hispanic, population in 2000 Census
- `H_BLACK`: Black, hispanic, population in 2000 Census
- `H_AMIN`: American Indian and Alaska Native, hispanic, population in 2000 Census
- `H_ASIAN`: Asian, hispanic, population in 2000 Census
- `H_NHPI`: Native Hawaiian and Pacific Islander, hispanic, population in 2000 Census
- `H_OTHER`: Other race, hispanic, population in 2000 Census
- `H_2MORE`: Two or more races, hispanic, population in 2000 Census
- `VAP`: Total voting age population in 2000 Census
- `HVAP`: Hispanic voting age population in 2000 Census
- `WVAP`: White, non-hispanic, voting age population in 2000 Census
- `BVAP`: Black, non-hispanic, voting age population in 2000 Census
- `AMINVAP`: American Indian and Alaska Native, non-hispanic, voting age population in 2000 Census
- `ASIANVAP`: Asian, non-hispanic, voting age population in 2000 Census
- `NHPIVAP`: Native Hawaiian and Pacific Islander, non-hispanic, voting age population in 2000 Census
- `OTHERVAP`: Other race, non-hispanic, voting age population in 2000 Census
- `CD10`: Congressional District ID for 2011 enacted plan
- `HDIST10`: State House District ID for 2011 enacted plan
- `SEND10`: State Senate District ID for 2011 enacted plan
- `CD00`: Congressional District ID for 2001 enacted plan
- `HDIST00`: State House District ID for 2001 enacted plan
- `SEND00`: State Senate District ID for 2001 enacted plan


Below is a brief description of each of the listed variables in the attribute table of the 2012-2016 shapefile:
- `DISTRICT`: Ward number/letter and precinct number/letter
- `NAME`: Precinct name
- `Shape_Le_1`: Length of feature
- `Shape_Area`: Area of feature 
- `TOWN`: Municipality name
- `WARD`: Ward number/letter, where applicable
- `PRECINCT`: Precinct number/letter
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
- `CD`: Congressional District ID for 2011 enacted plan
- `TOTPOP`: Total population in 2010 Census
- `NH_WHITE`: White, non-hispanic, population in 2010 Census
- `NH_BLACK`: Black, non-hispanic, population in 2010 Census
- `NH_AMIN`: American Indian and Alaska Native, non-hispanic, population in 2010 Census
- `NH_ASIAN`: Asian, non-hispanic, population in 2010 Census
- `NH_NHPI`: Native Hawaiian and Pacific Islander, non-hispanic, population in 2010 Census
- `NH_OTHER`: Other race, non-hispanic, population in 2010 Census
- `NH_2MORE`: Two or more races, non-hispanic, population in 2010 Census
- `HISP`: Hispanic population in 2010 Census
- `H_WHITE`: White, hispanic, population in 2010 Census
- `H_BLACK`: Black, hispanic, population in 2010 Census
- `H_AMIN`: American Indian and Alaska Native, hispanic, population in 2010 Census
- `H_ASIAN`: Asian, hispanic, population in 2010 Census
- `H_NHPI`: Native Hawaiian and Pacific Islander, hispanic, population in 2010 Census
- `H_OTHER`: Other race, hispanic, population in 2010 Census
- `H_2MORE`: Two or more races, hispanic, population in 2010 Census
- `VAP`: Total voting age population in 2010 Census
- `HVAP`: Hispanic voting age population in 2010 Census
- `WVAP`: White, non-hispanic, voting age population in 2010 Census
- `BVAP`: Black, non-hispanic, voting age population in 2010 Census
- `AMINVAP`: American Indian and Alaska Native, non-hispanic, voting age population in 2010 Census
- `ASIANVAP`: Asian, non-hispanic, voting age population in 2010 Census
- `NHPIVAP`: Native Hawaiian and Pacific Islander, non-hispanic, voting age population in 2010 Census
- `OTHERVAP`: Other race, non-hispanic, voting age population in 2010 Census
- `2MOREVAP`: Two or more races, non-hispanic, voting age population in 2010 Census
- `SEND`: State Senate District ID for 2011 enacted plan
- `HDIST`: State House District ID for 2011 enacted plan
- `NAME10`: Precinct name
- `GOV14R`: Number of votes for 2014 Republican gubernatorial candidate
- `GOV14D`: Number of votes for 2014 Democratic gubernatorial candidate
- `GOV14I`: Number of votes for 2014 United Independent Party gubernatorial candidate
- `GOV14U1`: Number of votes for 2014 Unenrolled gubernatorial candidate 1
- `GOV14U2`: Number of votes for 2014 Unenrolled gubernatorial candidate 2
- `GOV18R`: Number of votes for 2018 Republican gubernatorial candidate
- `GOV18D`: Number of votes for 2018 Democratic gubernatorial candidate
- `SEN18D`: Number of votes for 2018 Democratic senate candidate
- `SEN18R`: Number of votes for 2018 Republican senate candidate
- `SEN18U`: Number of votes for 2018 Unenrolled senate candidate

## Rating
We give these shapefiles an A rating. They come from either the Massachusett Secretary of the Commonwealth's office or the US Census Bureau. They were validated and edited by MGGG staff.
