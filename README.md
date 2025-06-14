[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/SdXSjEmH)
# EV-HW3: PhysGaussian


## Part1
Baseline sand, snow.  
<img src="PhysGaussian/output/sand/output.gif" width="30%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_n_grid_50/output.gif" width="30%" style="display:inline-block;">

## Part2
### Sand
#### n_grid:  
|10| 30 | 50 | 70 | 100|
|---|----|----|----|----|
|34.4361 |34.6917    |baseline| 34.772 | 34.2403 |

<img src="PhysGaussian/output/sand_n_grid_10/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand_n_grid_30/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand_n_grid_70/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand_n_grid_100/output.gif" width="18%" style="display:inline-block;">

#### substep_dt:
|5e-5 | 1e-4 | 2e-4|
|----|-------|----|
|34.4104|baseline|33.7762| 

<img src="PhysGaussian/output/sand_sub_step_dt_5e-5/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/sand/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/sand_sub_step_dt_2e-4/output.gif" width="30%" style="display:inline-block;">

#### grid_v_damping_scale: 
|0.999|0.9999|1|
|-|-|-|
|34.4987| baseline| 34.08|

<img src="PhysGaussian/output/sand_grid_v_999/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/sand/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/sand_grid_v_1/output.gif" width="30%" style="display:inline-block;">

#### softening:
|0.05|0.1|0.3|0.6|0.95
|-|-|-|-|-|
|48.1832| baseline| 51.6461| 46.5291 | 46.6113

<img src="PhysGaussian/output/sand_soft_0.05/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand_soft_0.3/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand_soft_0.6/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/sand_soft_0.95/output.gif" width="18%" style="display:inline-block;">



### Snow
#### n_grid:
|10| 30 | 50 | 70 | 100|
|-|----|----|----|----|
| 35.6909| 37.0375 | baseline| 37.3605 | 37.0354

<img src="PhysGaussian/output/snow_n_grid_10/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_n_grid_30/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_n_grid_50/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_n_grid_70/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_n_grid_100/output.gif" width="18%" style="display:inline-block;">


#### substep_dt:
|5e-5 | 1e-4 | 2e-4|
|----|-------|----|
|36.2175 | baseline | 37.0120

<img src="PhysGaussian/output/snow_substep_dt_5e_5/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/snow_n_grid_50/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/snow_substep_dt_2e_4/output.gif" width="30%" style="display:inline-block;">



#### grid_v_damping_scale: 
|0.999|0.9999|1|
|-|-|-|
|35.9077 | baseline | 37.3180

<img src="PhysGaussian/output/snow_grid_v_999/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/snow_n_grid_50/output.gif" width="30%" style="display:inline-block;margin-right:10px;">
<img src="PhysGaussian/output/snow_grid_v_1/output.gif" width="30%" style="display:inline-block;">

#### softening:
|0.05|0.1|0.3|0.6|0.95
|-|-|-|-|-|
|79.7885 |baseline| 78.6881 | 79.5434 | 79.1902

<img src="PhysGaussian/output/snow_soft_0.05/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_n_grid_50/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_soft_0.3/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_soft_0.6/output.gif" width="18%" style="display:inline-block;">
<img src="PhysGaussian/output/snow_soft_0.95/output.gif" width="18%" style="display:inline-block;">

## Analysis
### n_grid:
As the n_grid becomes larger, the resolution becomes greater. Hence, the simulation results would be more precise but simulation time is higher. Take sand as example. when n_grid is 10, it doesn't seem like sand. When n_grid is 100, it splits like sand.
### substep_dt:
As the substep_dt becomes larger, the faster it simulate but more unstable. Take sand as example. When substep_dt is 2e-4, the results are very exaggerate.
### grid_v_damping_scale: 
As the grid_v_damping_scale becomes larger, the result becomes unstable because it maintain the speed. When grid_v_damping_scale is small, the speed decay so it more likely maintain the original view. 
### softening: 
As the softening becomes larger, it theoretically should be more rigid and non fragile. However, it doesn't seem different in simulation video. 

## Key Takeaway

Although PhysGaussian supports a variety of materials, achieving visually realistic simulations still requires manual tuning of multiple physical parameters. Each material's behavior depends not only on the material type but also heavily on parameters like grid resolution, time step size, and damping. This manual process can be time-consuming and may limit the method’s scalability and usability in real-world scenarios. Automating parameter inference would significantly enhance the practicality of the framework. 

## Bonus 
One easiest way to replace manual human input is by using a LLM to infer physical parameters from the unfamiliar materials. However, if it doesn't work, maybe we can collect some data to fine-tune the LLM for better accuracy. 













This homework is based on the recent CVPR 2024 paper [PhysGaussian](https://github.com/XPandora/PhysGaussian/tree/main), which introduces a novel framework that integrates physical constraints into 3D Gaussian representations for modeling generative dynamics.

You are **not required** to implement training from scratch. Instead, your task is to set up the environment as specified in the official repository and run the simulation scripts to observe and analyze the results.


## Getting the Code from the Official PhysGaussian GitHub Repository
Download the official codebase using the following command:
```
git clone https://github.com/XPandora/PhysGaussian.git
```


## Environment Setup
Navigate to the "PhysGaussian" directory and follow the instructions under the "Python Environment" section in the official README to set up the environment.


## Running the Simulation
Follow the "Quick Start" section and execute the simulation scripts as instructed. Make sure to verify your outputs and understand the role of physics constraints in the generated dynamics.


## Homework Instructions
Please complete Part 1–2 as described in the [Google Slides](https://docs.google.com/presentation/d/13JcQC12pI8Wb9ZuaVV400HVZr9eUeZvf7gB7Le8FRV4/edit?usp=sharing).


# Reference
```bibtex
@inproceedings{xie2024physgaussian,
    title     = {Physgaussian: Physics-integrated 3d gaussians for generative dynamics},
    author    = {Xie, Tianyi and Zong, Zeshun and Qiu, Yuxing and Li, Xuan and Feng, Yutao and Yang, Yin and Jiang, Chenfanfu},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
    year      = {2024}
}
```
