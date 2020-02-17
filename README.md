# Continuous-time system identification with neural networks 

<!--- This repository contains the Python code to reproduce the results of the 
paper "Continuous-time system identification with neural networks" by Marco Forgione and Dario Piga. --->

The following fitting methods for continuous-time State-Space (SS) neural dynamical models are implemented

 1. Full simulation error minimization
 2. Truncated simulation error minimization
 3. Numerical discretization consistency


# Folders:
* [torchid](torchid):  pytorch models for several neural dynamical models
* [examples](examples): examples of neural dynamical models identification 
* [common](common):   definition of fitting metrics R-square, RMSE, fit index 

The [examples](examples) presented in the paper are:

* [RLC](examples/RLC): A simulated nonlinear RLC circuit 
* [CTS](examples/CTS): Cascaded Tanks System (CTS). Experimental data obtained from http://www.nonlinearbenchmark.org.
* [EMPS](examples/EMPS): Electro-Mechanical Positioning System (EMPS). Experimental data obtained from http://www.nonlinearbenchmark.org.

For the [Cascaded Tanks System](examples/CTS_example) example, the main scripts are:

 *  ``CTS_fit_truncated.py``: truncated simulation error minimization
 *  ``CTS_fit_consistency.py``: SS model, evaluate the simulation performance of the identified models, produce relevant plots  and model statistics
 *  ``CTS_eval_sim.py``: Evaluate simulation performance of the identified models
 *  ``CTS_OE_comparison.m``: Linear Output Error identification in Matlab (``oe`` method)
 *  ``CTS_subspace_comparison.m``: Linear subspace identification in Matlab (``n4sid`` method)
  

# Software requirements:
Simulations were performed on a Python 3.7 conda environment with

 * numpy
 * scipy
 * matplotlib
 * pandas
 * sympy
 * numba
 * pytorch (version 1.4)
 
These dependencies may be installed through the commands:

```
conda install numpy numba scipy sympy pandas matplotlib ipython
conda install pytorch torchvision cpuonly -c pytorch
```
