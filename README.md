This is an interactive plot of the survey of the Crystal Tree NSP locations on the Kepler Ridge. 
This survey was carried out mid 2025  
The initial visualisation is carried out locally using code not in this repository yet. 
The code uses python and pyvista to do data extraction and 3d renderings. The pyvista setof objects is saved as a gtlf file. 
This is called visualizations.gtlf and is uploaded 
The index.html js code then takes the gtlf file adds additional visualisation components and adds layer swicthes and an opacity slider to be able to adjust what the user looks
The user can rotate and view the visualisation.

Note there are 3 three.modules js files also added. This is because the modul.js files needed editing to remove "From Three" and replace with from (location below) 
from 'https://unpkg.com/three@0.154.0/build/three.module.js';
Those are are hardcoded with the local directory name , so if they get moved to another ropository will likely need some editing.

Note I did name the meshes in the python pyvista code with the intent to use those names here hwwever it didnt 'stick' so the meshes are called mesh0 mesh1 .....
I'll add some annotaions to explain what each one is if I can't get the name to export properly

Other work to do 
1) Add credits / title for IGAU spansh ,etc 
2) clean up axis labels and add coordinate ticks
3) clean up code for flow readbility - do i put lights cameras axis etc at the beginning or the end?
4) Add carrier locations if teh cmdrs will let me know where they were
5) Matt _G sphere and center point is good for showing the radius from a point 
6) Could add the convex hull visulisation but not needed probably ?
7) Animation of the survey over time - two pathes - do in pyvistasas movie of frame png files, or create seeveral gtml files at say weekly intervales and use a slider or something to alow user to step through
8) On animation simple one woudl be to do 'start' and 'ending' meshes . Should be easily doable from pyvista and have as start and incremenet layers  
