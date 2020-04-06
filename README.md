AutoNeuriteJ :

To install the macro you need to copy the text file called "Neuron.lut" inside the "Luts" folder of Fiji/ImageJ.

Note that tree other ImageJ/Fiji plugins are requested by the macro :
	
	The plugin "Analyze Skeleton 2D/3D" Developped by Ignacio Arganda-Carreras http://imagej.net/AnalyzeSkeleton 
	The plugin "MorphoLibJ" Developped by David Legland and Ignacio Arganda-Carreras https://imagej.net/MorphoLibJ 
	The plugin "Morphology" from Gabriel Landini's website : http://www.mecourse.com/landinig/software/software.html

Then you can run the macro entitled "AutoNeuriteJ (All in one)" with Fiji/ImageJ as an ".ijm" files.

More informations :

Running any part of the macro will ask for a few parameters to be filled such as location of your files directory, the size of the nucleus in your images, and keywords contained in the images names you want to analyse (in order to attribute the right image to nuclei staining and to neurons staining).
        
	- Part 1 : image pre-treatment of your images in order to enhance the segmentation efficiency of the neurons.

        - Part 2 : Pre-processing of your images in order to create stacks of all the neurons and the corresponding skeleton of these neurons.

        - Part 3 : Final quantification of the neurites.

Part 1 will ask you to select the threshold that fits the best your neuron staining (the same for the nucleus), so you will have to repeat this step as many times as you have images to analyze.
        
	Tips : Be careful to set the highest possible threshold in order to don't miss any thin neurites. 

Part 2 and 3 settings are already recorded to run properly with DIV2 hippocampal neurons, but could be adapted for other neurons types.
Part 2 and 3 are more automated so that different conditions (images) may be analyzed after indicating the directories containing all different files.

Important :

To properly use this macro, a directory is usually created for each condition with the two images corresponding to the neurons staining and the nucleus staining in each. All parts of the macro will create subfolders inside each directory necessary for the following steps. Note that for Part 2 and Part 3, the file directories requested by the macro correspond to those newly created subfolders. Part 3 will create a final subfolder in each, called "Measures", containing :
	
	- A stack of images named "Stack_of_Neurones": corresponding to the skeleton that had been measured, coded in different colors, depending on the hierarchy of the neurites (primary, secondary...).
        
	- A stack of images named "Overlay": corresponding to the original images of the neurons with the overlapping image of the skeleton that had been measured, coded in different colors, depending on the hierarchy of the neurites (primary, secondary...) --> this stack normally allows a visual check of the proper functioning of the macro.
        
	- A text file named "Values": that may be directly opened with Excel 
