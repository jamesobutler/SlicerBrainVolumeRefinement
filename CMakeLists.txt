cmake_minimum_required(VERSION 3.13.4)

project(BrainVolumeRefinement)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/BrainVolumeRefinement")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Antonio Carlos da S. Senra Filho, Fabricio H. Simozo, Luiz Otavio Murta Junior (University of Sao Paulo)")
set(EXTENSION_DESCRIPTION "This extension offers algorithms to performs brain volume refinements due to previous image processing that results on small data artifacts. For instance, the BVeR method is designed to correct small oversegmentation found at brain extraction methods such as FSL-BET, FreeSurfer, AFNI, ROBEX and others.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/CSIM-Toolkits/SlicerBrainVolumeRefinement/master/BrainVolumeRefinement.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/CSIM-Toolkits/SlicerBrainVolumeRefinement/master/T1_BET.png https://raw.githubusercontent.com/CSIM-Toolkits/SlicerBrainVolumeRefinement/master/T1_BET_BVeR.png https://raw.githubusercontent.com/CSIM-Toolkits/SlicerBrainVolumeRefinement/master/3D_BVeR_VolDiff.png https://raw.githubusercontent.com/CSIM-Toolkits/SlicerBrainVolumeRefinement/master/BVeR_gui.png")
set(EXTENSION_DEPENDS "NA") # Specified as a space separated string, a list or 'NA' if any

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(BVeR)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
