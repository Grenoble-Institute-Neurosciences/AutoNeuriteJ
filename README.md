AutoNeuriteJ
To install the macro you need to copy the text file called "Neuron.lut" inside the "Luts" folder of Fiji/ImageJ.
Run the macro entitled "AutoNeuriteJ (All in one)" with Fiji/ImageJ
Note that two other ImageJ/Fiji plugins are requested by the macro :
The plugin "Analyze Skeleton 2D/3D"  Developped by Ignacio Arganda-Carreras http://imagej.net/AnalyzeSkeleton
    the Morphology plugins from Gabriel Landini's website : http://www.mecourse.com/landinig/software/software.html

More information:
Running any part of the macro will ask for a few parameters to be filled such as location of your files directory, the size of the nucleus in your images or [keywords on your files naming in order to able the macro to determined witch image correspond to the neurons or to the nucleus.] J'ai pas compris ??

            - Part 1 : image pre-treatment of your images in order to enhance the segmentation efficiency of the neurons.

            - Part 2 : Pre-processing of your images in order to create stacks of all the neurons and the corresponding skeleton of these neurons.

            - Part 3 : Final quantification of the neurites.

Part 1 will ask you to select the threshold that fits the best your neuron staining (the same for the nucleus), so you will have to repeat this step as many times as you have images to analyze.
Part 2 will need no input from the user.
Part 3 is more automated so that different conditions (images) may be analyzed after indicating the directories containing all different files. Important :
To properly use this macro, a directory is usually created for each conditionwith  the two images corresponding to the neurons staining and  the nucleus staining in each.
All parts of the macro will create subfolders necessary for the following steps inside each diretory. Note that for Part 3, the file directories requested by the macro correspond to those newly created subfolders. It will create a final subfolder in each, called "Measures", containing;


            - a stack of images named "Stack_of_Neurones": corresponding to the skeleton that had been measured, coded in different colors, depending on the hierarchy of the neurites(primary, secondary...).
            - a stack of images named "Overlay": corresponding to the original images of the neurons with the overlapping image of the skeleton that had been measured, coded in different colors, depending on the hierarchy of the neurites(primary, secondary...) --> this stack normally allows a visual check of the proper functioning of the macro.
            - a text file named "Values": that may be directly opened with Excel 
