# VolumetricNeuralDeformableModels
This is the project page of volumetric neural deformable models (vNDMs) [[arXiv](https://arxiv.org/abs/2411.15233)].

## Learning Volumetric Neural Deformable Models to Recover 3D Regional Heart Wall Motion from Multi-Planar Tagged MRI.
We proposed a novel volumetric neural deformable model (vNDM) to recover the 3D regional heart wall motion from multi-planar [tagged-MRI](https://github.com/DeepTag/cardiac_tagging_motion_estimation). Our vNDMs represent heart wall geometry and motion through a set of low-dimensional global deformation parameter functions and a diffeomorphic point flow regularized local deformation field.
To learn such global and local deformation for 2D apparent motion mapping to 3D true motion, we design a hybrid point transformer, which incorporates both point cross-attention and self-attention mechanisms.
While use of point cross-attention can learn to fuse 2D apparent motion cues into material point true motion hints, point self-attention hierarchically organised as an encoder-decoder structure can further learn to refine these hints and map them into 3D true motion.
<div align=center><img width="820" height="221" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/vNDM.png"/></div>

## Demo 1
The following video shows simulated deforming left ventricle myocardium wall meshes across a full cardiac cycle.  
<div align=center><img width="300" height="300" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Mesh/simulation_mesh.gif"/></div>
<div align=center><img width="820" height="175.3" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Mesh/mesh_cardiac_cycle.png"/></div>

## Demo 2
The following videoes show the apparent Lagrangian motion sequences on SAX basal/middle/apical views (looking from base to apex) and LAX 2ch/3ch/4ch views. 
<div align=center><img width="250" height="237.4" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Apparent_Lagrangian_Motion/SAX/apparent_motion_sequence_sax_7.gif"/><img width="250" height="237.4" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Apparent_Lagrangian_Motion/SAX/apparent_motion_sequence_sax_5.gif"/><img width="250" height="237.4" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Apparent_Lagrangian_Motion/SAX/apparent_motion_sequence_sax_3.gif"/></div>
<div align=center><img width="250" height="238.6" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Apparent_Lagrangian_Motion/LAX/apparent_motion_sequence_lax_0.gif"/><img width="250" height="238.6" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Apparent_Lagrangian_Motion/LAX/apparent_motion_sequence_lax_1.gif"/><img width="250" height="238.6" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Simulation_Example/Apparent_Lagrangian_Motion/LAX/apparent_motion_sequence_lax_2.gif"/></div>

## Demo 3
The following videoes in the first row show the 3D regional heart wall motion recovery results by volumetric neural deformable models. The second row shows the ground truth deforming heart wall meshes. The first column shows the SPAMM datapoints on the SAX and LAX views. Starting from the second column, we show 5 layers of the heart wall, ranging from epicardial surface to endocardial surface.
<div align=center><img width="820" height="272.8" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/3D_Regional_Wall_Motion_Recovery_Example/supp_fig3_20_frames.gif"/></div>

## Demo 4
The following video and figure show the 3D regional endocardial heart wall motion recovery results from real 2D tagged cardiac cine MRI stacks by volumetric neural deformable models. Note the complex back-and-forth twisting motion patterns at the basal wall region.
<div align=center><img width="300" height="300" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Real_Tagged_Cine_MRI_Results/5_recon_endocardial_wall.gif"/></div>
<div align=center><img width="820" height="204.5" src="https://github.com/DeepTag/VolumetricNeuralDeformableModels/blob/main/Real_Tagged_Cine_MRI_Results/recon_endo_regional_motion_cycle.png"/></div>

