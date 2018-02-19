
skipExistingData = no
# skipExistingData = yes

import_land:
	grass GRASSDATA/AA/PERMANENT --exec ./importLand.grass $(skipExistingData)

import_adm:
	grass GRASSDATA/AA/PERMANENT --exec ./importAdm.grass $(skipExistingData)


# dissolve_land: import_land
	# grass GRASSDATA/epsg4326/PERMANENT --exec ./dissolveLand.grass $(skipExistingData)
	

# reproj_land: dissolve_land
	# grass GRASSDATA/AA/PERMANENT --exec ./reprojLand.grass $(skipExistingData)

# del_landCats: reproj_land
	# grass GRASSDATA/AA/PERMANENT --exec ./dropCats.grass $(skipExistingData)

prepare_data: import_land import_adm


simplify: prepare_data
	grass GRASSDATA/AA/PERMANENT --exec ./simplify.grass $(skipExistingData)
