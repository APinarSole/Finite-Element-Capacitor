This script implements a finite element method to model a plate capacitor and a point charge inside using the relaxation method. The method iteratively solves Laplace's equation to determine the potential distribution between the capacitor plates. The script provides three main outputs:
1. A contour plot of the potential (V) at the midplane.
2. The capacitance (C) as a function of plate separation.
3. The potential (V) at the center as a function of plate separation.

The accuracy of the simulation improves with higher iteration counts and increased point density, but at the cost of longer computation times. Care should be taken not to set excessively large plate sizes, as this can significantly slow down calculations.

## How to Use the Code
1. **Set Parameters:**
   - `V0 = 1`        # Potential difference between plates (V)
   - `q = 0`         # Point charge in elementary charge units
   - `L = 1`         # Side length of capacitor plates (m)
   - `d = 1.4`       # Initial plate separation (m)
   - `point_density = 100`  # Resolution of the grid (points per meter)
   - `size_grid = 2` # Lateral size of the simulation grid (m)
   - `da = 0.1`      # Distance between the atom and the plate (m)
   - `width = 0.1`   # Thickness of the plates (m)
   - `iterations = 30` # Number of iterations for the relaxation method
   - `divisions = 10` # Number of points to sample for z-dependence of potential

2. **Run the Script:**
   - The script solves for the potential distribution using the relaxation method.
   - A contour plot of the potential at the midplane is generated.
   - The potential at the center and the capacitance as a function of plate separation are computed and plotted.
   
3. **Interpreting Results:**
   - The contour plot visualizes how potential varies in the capacitor.
   - The potential at the center and capacitance are displayed for various plate separations.
   - The script prints key data, such as computed capacitance values and execution time.

**Notes:**
- Increasing the number of iterations and point density improves the accuracy of the results but also increases computation time.
- Ensure that the plate size (`L`) is not excessively large relative to the grid size (`size_grid`) to avoid excessive computation.
