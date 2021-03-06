# Skeletonization
Tracking c. elegans can become quite a challenge, when these worms roll up in coiled shapes, aggregate with other worms, or with dirt in the petri dish. In this work, a simple solution is proposed using artificial vision techniques to help tracking these nematodes. This method uses the distance transform function to obtain an improved skeleton. Using this new skeleton some possible predictions of the next pose are obtained. An optimization function evaluates all and determines the best next pose prediction.

# Requirements:
This demo was tested in Windows 10 with Matlab R2018b.
- Windows 10
- Matlab R2018b
- Image Processing Toolbox
- Communications Toolbox
- Bioinformatics Toolbox

# Clone Skeletonization repository:
```
git clone https://github.com/playanaC/Skeletonization.git
```

# Run the skeletonization demo in Matlab:
- Before you start, change the path of the images in *path variable* in Main.m file.
- If you want to skip the track processing part, you could uncomment lines 7,8, and comment lines 10 through 21 or vice versa.
- Run Main.m macro. This macro will first find the region of interest (inside the petri dish), then it will get all the worm trajectories, these will be evaluated to classify the areas in worm tracks(red), noise (blue), areas with little movement (green). Second, you will evaluate each tracks to obtain all the worm skeletons within it. Third, the results will be saved in xml files. 

# Run Gui_viewer in Matlab:
Gui_viewer is an app to view the results saved in xmls files.
- First you must select the path of the images with the xmls files using *Path* button.
- Second in *button group* at the bottom you must select one of the options.
- Third, if *Single worm* was selected, one of the xml files must be selected, and then one of the images should be selected to see the skeleton in image 1 and in image 2 with increased resolution.
- If *All worms* was selected, only one of the images should be selected to see all the worm skeletons. At the top, you can select *Zoom in* to get a closer look at each skeleton in image 1.

# Image adquisition system:
- Images were captured by an [open hardware system](https://github.com/JCPuchalt/c-elegans_smartLight).


# References:
- Puchalt, J. C., Sánchez-Salmerón, A.-J., Martorell Guerola, P. & Genovés Martínez, S. "Active backlight for automating visual monitoring: An analysis of a lighting control technique for *Caenorhabditis elegans* cultured on standard Petri plates". PLOS ONE 14.4 (2019) [doi paper](https://doi.org/10.1371/journal.pone.0215548)

- Puchalt, J.C., Sánchez-Salmerón, A., Ivorra, E. et al. "Improving lifespan automation for *Caenorhabditis elegans* by using image processing and a post-processing adaptive data filter". Scientific Reports (2020) [doi paper](https://doi.org/10.1038/s41598-020-65619-4).

- Layana Castro Pablo E., Puchalt, J.C., Sánchez-Salmerón, A. "Improving skeleton algorithm for helping *Caenorhabditis elegans* trackers". Scientific Reports (2020) [doi paper](https://doi.org/10.1038/s41598-020-79430-8).

# Citation:
```
@article {Layana2020,
  Title = {Improving skeleton algorithm for helping *Caenorhabditis elegans* trackers.},
  Author = {Layana Castro, Pablo E. and Puchalt, Joan Carles and Sánchez-Salmerón, Antonio-José},
  DOI = {https://doi.org/10.1038/s41598-020-79430-8},
  Pages = {22247}, 
  Number = {1},
  Volume = {10},
  Month = {May},
  Year = {2020},
  journal = {Scientific Reports}
  }
```
