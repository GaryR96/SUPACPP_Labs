This repository contains a complete solution for the second SUPAC++ assignment:

- Use the provided `FiniteFunctions` base class to explore finite functions or use the one that I have already made. 
- Add new distributions (`Normal`, `Cauchy–Lorentz`, `Crystal Ball`) via inheritance.
- Use the Metropolis algorithm to sample from the distribution you believe generated the data in `MysteryDataXXXXX.txt`.

## Files

### Core classes

- `FiniteFunctions.h` – declaration of the base class `FiniteFunctions`.
- `FiniteFunctions.cxx` – implementation of `FiniteFunctions`:
  - default function `f(x) = 1 / (1 + x^2)`,
  - numerical integration on a finite interval,
  - automatic normalisation,
  - file output for plotting,
  - Metropolis sampler usable by all derived classes.

- `Distributions.h` – declarations of:
  - `NormalFunction` (Gaussian),
  - `CauchyLorentzFunction`,
  - `CrystalBallFunction`.

- `Distributions.cxx` – implementations of the three distributions using the formulas from the assignment.

### Main analysis program

- `main.cxx` – executable that:
  1. Reads the mystery data from `Output/Data/MysteryDataXXXXX.txt`.
  2. Computes the range, mean and standard deviation of the data.
  3. Chooses sensible limits `[xmin, xmax]` (data range with a margin).
  4. Constructs:
     - the default `FiniteFunctions` object,
     - `NormalFunction`,
     - `CauchyLorentzFunction`,
     - `CrystalBallFunction`.
  5. Prints the integral and normalisation factor for each function.
  6. Writes normalised function values to:
     - `default_function.dat`,
     - `normal_function.dat`,
     - `cauchy_function.dat`,
     - `crystalball_function.dat`.
  7. Copies the input data to `mystery_data.dat` for easy plotting.
  8. Uses the Metropolis algorithm (implemented in `FiniteFunctions`) to:
     - sample new points from the **Crystal Ball** distribution (the chosen model),
     - write them to `metropolis_samples.dat`.

#############################################################################################################

Also, because it seemed better to me, I've made a new 'main' that contains everything, all in one, 
and if you compile it, it generates and runs everything that needs to be generated. Try it if you want!!!