This is an interactive plot of the bubble expansion colonisation for Elite Dangerous 
All data from Spansh and edgalaxydata.space and eveyone who contributes via the eddn network.  
https://spansh.co.uk/dumps
https://edgalaxydata.space/

The initial visualisation is carried out locally using code not in this repository yet. 
The code uses python and pyvista to do data extraction and 3d renderings. The pyvista setof objects is saved as a gtlf file. 
This is called visualizations.gtlf and is uploaded 
The index.html js code then takes the gtlf file adds additional visualisation components and adds layer swicthes and an opacity slider to be able to adjust what the user looks
The user can rotate and view the visualisation.

Note there are 3 three.modules js files also added. This is because the modul.js files needed editing to remove "From Three" and replace with from (location below) 
from 'https://unpkg.com/three@0.154.0/build/three.module.js';
Those are are hardcoded with the local directory name , so if they get moved to another ropository will likely need some editing.

Note I did name the meshes in the python pyvista code with the intent to use those names here however it didnt 'stick' so the meshes are called mesh0 mesh1 .....
I'll add some annotaions to explain what each one is if I can't get the name to export properly from pyvista.
On further investigation it appears pyvista does not support exporting mesh names

Pathways - either need to figure out how to complete teh visulisation in pyvista and export the meshes complete so i dont have to mess with them in JS. or I just need to export dat as csv or some file , and do the full render pass in three.js 
I am lening toward everything in three.js 

Other work to do 
1) Add credits / title for IGAU spansh edgalaxydata,etc 
2) Add key for systems 
3) Add nebula check correct places
4) Need to verify what is going on with x y z coordinates - is three.js using a left or right hand coordinate system? Seems like their Y is 'up down' same as ED , but Z maybe 'left right and X in out - to be verified 
5) Need to add IGAU and mayme mercs of mikkum as a set. Need ot see where in the spansh dump the mirnor faction in control of the system is listed . is it part of the system meta data with the main  allegiance power or burried in the station data
6) If i don't wan't to redo the whole extraction I can likly get a seperate csv from spansh website and then lookup and replace those in the python / pyvista routine
7) Add moving focus ball, so as the camera focus is moved the focal point sphere moves
8) Improve the before / after switch either wording or implement toggle switch
9) Add KDE surfaces for system control - It should be a single switch in the UI to enable or disable which is dependent on the faction selected switch. Need to see how KDE meshes export from PYvista and render in three.js. May or maynot be too much data 
