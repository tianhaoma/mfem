# Install mfem-ma


## download mfem-ma
$ git clone https://github.com/tianhaoma/mfem-ma.git  
$ cd mfem-ma  
$ git checkout mesh-GridFunction-partitioner-dev  


## build MFEM: https://mfem.org/building/
### modify the hypre DIR in file config/default.mk
(use metis-5 or not)  
$ make parallel MFEM_USE_METIS_5=YES METIS_DIR=<dir-to-metis-5>  
$ cd mfem-ma/miniapps/meshing  
$ make mesh-explorer  

## Prepare .vtk .fiber .sheet .transverse to extract them into parallel.

$ ./mesh-explorer -m <dir-to-mesh> -gf_f <dir-to-.fiber> -gf_s <dir-to-.sheet> -gf_t <dir-to-.transverse>  


