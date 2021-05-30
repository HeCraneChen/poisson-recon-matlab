# PoissonSurfaceReconstruction_MATLAB-Version

This repo includes Poisson Surface Reconstruction code in MATLAB mostly. For the MarchingCubes function, we used Python skimage package.

# Usage
Download data from the following link, Unzip it into the code folder, so that all data should be stored in"PoissonSurfaceReconstruction_MATLAB-Version/Data", and the code should run, no other changes required.

https://drive.google.com/drive/folders/1kKZinGw09bzwPw-0wMcZhhJJJDEZAMEu?usp=sharing

# Requirements
For Matlab code, Matlab2019A or whatever version.

For Marching Cubes, Visualization, and Uniformly sampling oriented points from a PLY file, need to create a Conda environment or Virtual environment of Python3 and install the following libraries.

Numpy

Scipy

Skimage

Trimesh

Open3D


# Some Results in 2D

Direct (run ElephantSolver.m) --res 128 

![Elephant_Direct](https://user-images.githubusercontent.com/33951209/118314648-441a9e80-b4a9-11eb-8a5c-9facee7713b0.jpg)

Jacobi (run IterativeElephantSolver.m) --res 128 --iter 100 

![Elephant_Jacobi](https://user-images.githubusercontent.com/33951209/118314707-5a285f00-b4a9-11eb-8cad-3a0bdd397b08.jpg)

Gauss-Seidel (run IterativeElephantSolver.m) --res 128 --iter 100 

![Elephant_GaussSeidel](https://user-images.githubusercontent.com/33951209/118314722-5e547c80-b4a9-11eb-8ed1-23798654f402.jpg)

Multigrid (run IterativeElephantSolver.m) --res 128 --iter 10

![Elephant_Multigrid](https://user-images.githubusercontent.com/33951209/118314731-614f6d00-b4a9-11eb-901b-0e36b06052f9.jpg)

Ground truth grid
![gt_grid](https://user-images.githubusercontent.com/33951209/118325601-8c8d8880-b4b8-11eb-80d0-9e194c620c38.jpg)

Numerical Error (gt_grid - output/ mean(output, 'all') * mean(gt_grid, 'all'))

![num_error](https://user-images.githubusercontent.com/33951209/118326157-6fa58500-b4b9-11eb-954b-f0b240353ff8.jpg)

isovalue = -8.4444e-04

# Some Results in 3D (Slices)

Reconstructed
![reconstruted](https://user-images.githubusercontent.com/33951209/118333176-260c6880-b4c0-11eb-88e6-d9fb7dd49b08.jpg)

Version1 (run IterativeFoxSolver_v1) --res 128 --iter 10

Ground truth grid
![gt_v1](https://user-images.githubusercontent.com/33951209/118333359-6bc93100-b4c0-11eb-973d-6d7ea3dd30ee.jpg)

Numerical Error (gt_grid - output/ mean(output, 'all') * mean(gt_grid, 'all'))
![error](https://user-images.githubusercontent.com/33951209/118333619-e003d480-b4c0-11eb-961d-cf85aeba834a.jpg)

Version2 (run IterativeFoxSolver_v2) --res 128 --iter 10

Ground truth grid
![gt_v2](https://user-images.githubusercontent.com/33951209/118334771-18a4ad80-b4c3-11eb-8c99-78e090b31331.jpg)

Numerical Error (gt_grid - output/ mean(output, 'all') * mean(gt_grid, 'all'))
![error_v2](https://user-images.githubusercontent.com/33951209/118334784-1e01f800-b4c3-11eb-895d-5b6b9a00c3a0.jpg)

Version3 (run IterativeFoxSolver_v3) --res 128 --iter 10

Ground truth grid
![gt_v3](https://user-images.githubusercontent.com/33951209/118335706-12afcc00-b4c5-11eb-8b17-97c68a0c5b08.jpg)

Numerical Error (gt_grid - output/ mean(output, 'all') * mean(gt_grid, 'all'))
![error_v3](https://user-images.githubusercontent.com/33951209/118335719-193e4380-b4c5-11eb-89c1-36328b18e28e.jpg)

# Some Results in 3D (The surface after marching cubes)

Results using sparse matrix + Direct Method. --res 64
![Slice1_64](https://user-images.githubusercontent.com/33951209/119586598-e415d900-bd81-11eb-9fce-8cf446f1544d.jpg)
![Slice2_64](https://user-images.githubusercontent.com/33951209/119586559-cf394580-bd81-11eb-9cb0-c591c8c98878.jpg)
![Slice3_64](https://user-images.githubusercontent.com/33951209/119586612-eaa45080-bd81-11eb-8d8f-66fb9e2d9078.jpg)
![SparseDirect](https://user-images.githubusercontent.com/33951209/119586565-d2cccc80-bd81-11eb-9033-cfdca60bf4b5.jpg)

Results using sparse matrix + Gauss Seidel --res 64 --iter 100
![Slice1_Gauss](https://user-images.githubusercontent.com/33951209/120114507-4da43780-c134-11eb-8a95-58568c80039c.jpg)
![Slice2_Gauss](https://user-images.githubusercontent.com/33951209/120114519-5b59bd00-c134-11eb-8232-2e2147a48030.jpg)
![Slice3_Gauss](https://user-images.githubusercontent.com/33951209/120114530-69a7d900-c134-11eb-869a-268db8bb5407.jpg)

Results using sparse matrix + Multigrid   --res 64 --iter 10
![Slice1_Multigrid](https://user-images.githubusercontent.com/33951209/120114512-53018200-c134-11eb-83ed-408b8d0696ef.jpg)
![Slice2_Multigrid](https://user-images.githubusercontent.com/33951209/120114523-5f85da80-c134-11eb-8d9f-9ed666d3a265.jpg)
![Slice3_Multigrid](https://user-images.githubusercontent.com/33951209/120114536-72001400-c134-11eb-91d6-765616700ff5.jpg)


# Results of C++ code
![2](https://user-images.githubusercontent.com/33951209/118743313-fedad180-b806-11eb-8d30-e23750864277.jpg)

