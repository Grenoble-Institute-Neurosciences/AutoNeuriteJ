AutoNeuriteJ :

To install the macro you need to copy the text file called "neurons.lut" inside the "Luts" folder of Fiji/ImageJ.

Note that tree other ImageJ/Fiji plugins are requested by the macro :
	
	The plugin "Analyze Skeleton 2D/3D" Developped by Ignacio Arganda-Carreras http://imagej.net/AnalyzeSkeleton (By default in Fiji)
	The plugin "MorphoLibJ" Developped by David Legland and Ignacio Arganda-Carreras https://imagej.net/MorphoLibJ (in Fiji : check "IJBP-Plugins" in the Update site window).
	The plugin "Morphology" from Gabriel Landini's website : http://www.mecourse.com/landinig/software/software.html (in Fiji : check "Morphology" in the Update site window).

Then you can run the macro entitled "AutoNeuriteJ.ijm" with Fiji/ImageJ.
Or use the macro entitled "AutoneuriteJ-for-mac.ijm" if you're using a mac.

More informations :

Running any part of the macro will ask for a few parameters to be filled up such as location of the files you want to analyze, keywords in their names, and different parameters concerning the size of the nucleus andd neurites.
        
	- Part 1 : image pre-treatment for enhancing the segmentation efficiency of the neurons.

        - Part 2 : Pre-processing of segmented images to create stacks of individual neurons and their skeleton.

        - Part 3 : Measurement of neuritic length and classification.

Part 1 will ask you to select the threshold that fits the best your neuron and nuclei.  
so you will have to repeat this step as many times as you have images to analyze.
        
	Tips : Be careful to set the low limit of the threshold really low to get a maximum of neurite (one click above 0).
	for the nuclei, the staining is homogenous so you may have to do nothing for the threshold.

Part 2 and 3 settings are recorded to run properly with DIV2 hippocampal neurons, but could be adapted for other type of neurons .
Part 2 and 3 are more automated so that different images may be analyzed after indicating their directories path ( one directory per image to analyze).

Recommended settings for hippocampal neurons at 1µm/pxl resolution :

	-Part I :
		- Minimal area for a neuron (in pixels) : 1500
		- Nucleus diameter (in pixels) : 30			
	-Part II :
		- Minimal skeleton length of a neuritic tree (in pixels) : 15
		- Minimal area for a binary Neuron (in pixels) : 2000
		- Minimal total skeleton length to consider a neuron (in pixels) : 100
	-Part III :
		- Minimal size for a Neurite (in pixels) : 15
		- Minimal size for an Axon (in pixels) : 150
		- Ratio (Axon Length)/(Longest Primary Neurites length) to be an Axon : 1.3 to 2


Important :

To properly use this macro, a directory is usually created for each condition with the two images corresponding to the neurons staining and the nucleus staining. All parts of the macro will create subfolders inside each directory necessary for the subsequent steps. Note that for Part 2 and Part 3, the directories requested by the macro correspond to the newly created subfolders. Part 3 will create a final subfolder, called "Measures", containing :
	
	- A stack of images named "Stack_of_Neurites": corresponding to the skeletons that had been measured, coded in different colors, depending on the hierarchy of the neurites (primary, secondary...).
        
	- A stack of images named "Overlay": corresponding to the original images of the neurons with the overlapping image of the skeleton, with the same color code than above --> this stack normally allows a visual check of the proper functioning of the macro.
        
	- A text file named "Results": that can be processed in a spreadsheet (e.g. Excel)
