# Axon_Segmentation
Automated pipeline for segmentation of axons in SMI-31 stained post-mortem spinal cord tissue 

QuPath with StarDist and heavy_pb model is required.

Steps for performing pipeline:
1. Open images in Qupath, model is designed for SMI-31 stained tissue with image set to "Brightfield-Other"
2. run Spheroid_Large_axon_QuPath as script in QuPath - segments spheroids and large caliber axons
3. run medium_Axon_seg_QuPath as script in QuPath - segments medium caliber axons
4. run small_axon_seg_QuPath as script in QuPath - segments small caliber axons
5. Export detections as CSV file 
6. Run Axon_density_metric_map_MATLAB in matlab to convert CSV file entries into cell arrays and grayscale images of axon densities per pixel
