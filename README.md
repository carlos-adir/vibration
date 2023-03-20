# Vibrações

**Versão em português [aqui](https://github.com/carlos-adir/vibration/blob/main/README.md)**

## Abstract

This folder containts codes made for vibrations course at UnB. 
Briefly, the dynamic ODE is given by

$$m \ddot{x} + c \dot{x} + k x = f$$

There are the cases:

* Modeling:
    * Get analitic EDO from real problem
* Free vibration (```f = 0```):
    * Analitic solve this equation.
    * Implement numerical solution
* Harmonic vibration (```f = f0*exp(i*w*t)```):
    * Analitic solve the equation
    * Implement numerical solution
    * Frequency analisis of system
* Non-oscilatory vibration (```f``` transient):
    * Analitic solve using Laplace transformation
    * Implement numerical solution
* Multi Degrees of freedom system:
    * Modal decomposition
    * Dynamic vibration absorber
* Experimental: Estimate parameters
    * Free vibration experiment
    * Harmonic vibration experiment

Some documents are written in English (indicated with ```EN```) and others are in Portuguese (```BR```).

## Documents

* Homework
    * ```BR``` - ```Homework/1_VigaMassaEquivalente.pdf```: Given a beam with bending stiffness ```EI``` and linear density ```mu```, we estimate the equivalent mass ```m``` and spring constant ```k``` of the first modal frequency.
    * ```BR``` - ```Homework/2_EquacoesGovernantes.pdf```: Model a cilinder + spring to find system's ODE using the Lagrange mechanics differential formulation.
    * ```EN``` - ```Homework/3_DropMass.ipynb```: Model the colision of an free object into another conected into a spring-damper.
    * ```BR``` - ```Homework/4_MassaDesbalanceada.pdf```: Model a unbalanced helicopter propeller which rotates with angular speed ```w```.
    * ```EN``` - ```Homework/5_VaribleForce.ipynb```: Find the position ```x``` of a mass-spring-damper system with force ```f``` decomposed in ```step``` and ```ramp``` using laplace transform.
* Experimental
    * ```BR``` - ```Experimental/first_experiment/```: Using a hammer on a cantilever beam, we find vibrational parameters ```xi``` and ```wn``` from exponential decay response ```a``` mesured by an accelerometer. Uses the ```estimate-exponential-decay.ipynb``` theory.
    * ```BR``` - ```Experimental/second_experiment/```: Using a cantilever beam connected with a oscilating piston at its end, we find parameters ```m```, ```c``` and ```k``` from the timed graphs of ```f```(force) and ```a```(acceleration) with different frequencies. Uses the ```estimate-forced-harmonic.ipynb``` theory.
* ```EN``` - ```dynamic-vibration-absorber.ipynb```: Transform a 1 DOF system into a 2 DOF system to minimize the gain ```X1``` of a mass-spring-damper system (```m1```, ```c1```, ```k1``` fixed) by adding another mass-spring-damper system (```m2```, ```c2```, ```k2``` variable)
* ```EN``` - ```estimate-exponential-decay.ipynb```: Using a 'mesured' (artificial generated noisy data) timed exponential decay response ```a``` of 1 DOF mass-sprint-damper system, we find the best parameters ```xi``` and ```wn``` to fit the curve using non-linear least square method with newton's iteration. Made for the ```first_experiment```.
* ```EN``` - ```estimate-forced-harmonic.ipynb```: Using 'mesured' (artificial generated noisy data) force ```f``` and acceleration ```a``` with different frequencies ```w```  of a 1 DOF mass-spring-damper system, we find the best values for ```m```, ```c``` and ```k``` of this system using least square method to fit the curves. Made for the ```second_experiment```.
* ```BR``` - ```forcamento-harmonico.ipynb```: From a 1 DOF mass-spring-damper system with applied harmonic force ```f0*exp(i*w*t)```, we compute the analitical and numeric response from given parameters  ```m```, ```c``` and ```k``` and initial conditions ```x0``` and ```v0```.
* ```BR``` - ```sistema-massa-mola.ipynb```: Using a free (```f=0```) mass-spring-damper system with parameters ```m```, ```c``` and ```k``` and initial conditions ```x0``` and ```v0```, we compute the analitical and numeric response.
* ```EN``` - ```multi-dofs-system.ipynb```: Has the theory and the numerical implementation and modal decomposition for a ```N``` DOFs system.
