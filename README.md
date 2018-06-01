# AutoNeuriteJ 

To install the macro you only need to separately copy :

                                _ The 3 parts of the macro in the "macros" folder of Fiji/ImageJ under the names AutoNeuriteJ_Part0.ijm ; AutoNeuriteJ_Part1.ijm ; AutoNeuriteJ_Part2.ijm
                                _ The text file called "AutoRun AutoneuriteJ.ijm" inside the "toolsets" folder inside the "macros" folder of Fiji/ImageJ.
                                _ The text file called "Neuron.lut" inside the "Luts" folder of Fiji/ImageJ.
                                
        
You will find the macro inside the ">>" button on the right of Fiji/imageJ toolbar. 3 buttons (0; 1; 2) will appear and correspond to itch part of the macro.
                                

Note that 2 others ImageJ/Figi plugins are requested by the macro :

        The plugin "Analyze Skeleton 2D/3D"  Developped by Ignacio Arganda-Carreras http://imagej.net/AnalyzeSkeleton
        the Morphology plugins from Gabriel Landini's website : http://www.mecourse.com/landinig/software/software.html
        
        
        
More informations:

Running of any parts of the macro will ask you few questions such as location of your files directory, the size of the nucleus of your images or keywords on your files naming in order to able the macro to determined witch image correspond to the neurons or to the nucleus.

                - Part 0 : image pre-treatment of your images in order to enhance the segmentation efficiency of your neurons.

                - Part 1 : Pre-processing of your images in order to create stacks of all your neurons and the corresponding skeleton of those neurons.

                - Part 2 : Correspond to the final quantification of the neurites.

Part 0 will ask you to select the threshold that fits the best to your neuron staining (the same for the nucleus), so you will have to repeat this part as many time as you have different images to analyze.

Part 1 and 2 or more automated so you will be able to say to the macro that you have different conditions (images) to analyze and once you gave to the macro the directories of all the different files it will run automatically those files one after the other.

 

Most important ! :

To proper use this macro, I usually create a folder for each conditions with inside the folder the two images corresponding respectively to the neurons staining and to the nucleus staining.

All parts of the macro will create inside the folder of the images another folder necessary for the next step of the macro. Be careful for all parts the file directories requested by the macro correspond to those folder.  

Finally you will find last folder inside called "Mesure" containing :

                - a text file : that you can directly open on excel (I am not sure that the naming of each rows are already translated in english, please ask me if not)

                - a stack of images : corresponding to the original images of the neurons that had been quantified.

                - a stack of images : corresponding to the original images of the neurons with the overlapping image of the skeleton that had been measured coded in different colors in function of the order of the neurons (primary, secondary...) --> this stack normally allows a visual check of the proper functioning of the macro!
