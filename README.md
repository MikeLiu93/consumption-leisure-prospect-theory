# consumption-leisure-prospect-theory
Consumption and leisure, prospect theory (reference-dependent utility), EGM

Model6_CL (VFI) solves the model with two decision variables (consumption and leisure), two state variables (exogenous reference level and endogenous updating wealth), and reference-dependent utility function using VFI method. Only 1D interpolation is required.
Model6_CL (EGM) solves the same problem using EGM.

Model6_CL_sim (VFI) and Model6_CL_sim (EGM) simulate the optimal results provided above under uncertain investment returns. The difference is that simulation requires 2D interpolation on wealth and reference level. Policy functions with VFI are on regular grids, which can be solved using bilinear interpolation. Howver, policy functions with EGM are on irregular grids, which can create some problems. (interpolate.Rbf is extremely slow)

CL_3.1.6 and CL_3.2.3 are fundamentally different from model 6, now reference level becomes and endogenously updating state variable instead of a steady one. Thus the optimization process also requires 2D interpolation. 
For now I use Rbf as there are no existed suitable packages. However a more suitable interpolation method can be created to fill the gap.
Optimisation is half-finished and no simulation is provided for now.
