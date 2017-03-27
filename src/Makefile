######################################################################
# Subsamples netCDF file in space given a set of lat, lon boundaries:
#  		LATMIN, LATMAX, LONMIN, LONMAX
#  Please adjust the paths accordingly
######################################################################


CCMPDIR = /Users/bia/work/projects/python/python_basics/data/ccmp/2010/01
CCMPSUFIX = _v11l30flk.nc
CCMPFILES = `ls $(CCMPDIR)/*$(CCMPSUFIX)`
OUTDIR = /Users/bia/work/projects/python/python_basics/data/ccmp_california


LATMIN = 22.0
LATMAX = 47.0
LONMIN = 220.0
LONMAX = 255.0

space_crop:
	for file in $(CCMPFILES); do \
	     filename=`basename $$file`; \
	     ncks -d lat,$(LATMIN),$(LATMAX) \
	     -d lon,$(LONMIN),$(LONMAX) \
             $$file $(OUTDIR)/$$filename; \
	done
