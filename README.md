This is an interactive plot of the bubble expansion colonisation for Elite Dangerous 

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
1) Add credits / title for IGAU spansh edgalaxydata,etc 
2) many many things 
