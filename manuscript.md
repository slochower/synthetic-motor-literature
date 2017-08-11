---
author-meta:
- David R. Slochower
date-meta: '2017-08-11'
keywords:
- work-in-progress
- markdown
- manuscript
- publishing
title: Synthetic molecular motors
...

<small><em>
This manuscript was automatically generated
from [slochower/synthetic-motor-literature@d94a4ed](https://github.com/slochower/synthetic-motor-literature/tree/d94a4edcf80d074ec8005f09ba9f74390920a0f6)
on August 11, 2017.
</em></small>


## Commentary on "Intramolecular torque, an indicator of the internal rotation direction of rotor molecules and similar systems" [@xZIRNGMm]

In this paper, intramolecular (atomic) torque is defined using a classical analog, namely $\mathbf{\tau} = \mathbf{F} \times \mathbf{r}$, and the total torque on the molecule as the vector sum of individual atomic torques.
The stator is held rigid and the reference point for the torque calculation is the double bond between the stator and the rotor.
The forces arise from photoexcitation of the double bond -- the so-called [Franck-Condon](https://en.wikipedia.org/wiki/Franck%E2%80%93Condon_principle) state that is referenced in several of Feringa's papers -- where the moolecule is in an *electronic* excited state (S1) but the atomic coordinates are in the ground state (S0).
That is, there is strain on the roto due to the photoexcitation and the chirality of the molecule that prevents free rotation.
I also think this inability to rotate upon excitation is what is meant by the name "overcrowded alkene," although it seems not all ring substituents leads to overcrowding.

I'm not sure there is anything wrong with this approach, per se, but it seems simplistic and that it could miss out a lot of confounding effects; that the stator is modeled as rigid is one assumption, another assumption is zero temperature.
The authors used DFT to calculate the Franck-Condon state every couple degrees, noting that when the $\ce{C=C}$ double bond is near 85 degrees, the ground state and excited state energies are similar.
Around that angle, I think, they then allow the geometry to switch from the excited state (S1) back to the ground state (S0) and continue the calculation, confirming continuous counterclockwise rotation.
Taken together, I don’t find this paper very clear or convincing, but I might not be evaluating it fairly.

References 28 and 29 in [@xZIRNGMm] are [@N6pRFM85] and [@so4s7d25] respectively.

### Commentary on reference 28 from [@xZIRNGMm] -- "Understanding the Dynamics Behind the Photoisomerization of a Light-Driven Fluorene Molecular Rotary Motor" [@N6pRFM85]
[@N6pRFM85] calculates the ground and excited state potential energy surfaces of a typical four-stroke Feringa-type motor using DFT yielding "unprecedented understanding of the photoisomerization process."
This paper introduces the term [conical intersection](https://en.wikipedia.org/wiki/Conical_intersection) which I gather to mean the overlap (non-adiabatic, vibronic coupling) between the excited and ground state potential energy surfaces.
This paper says that breaking of the double bond is necessary to switch helicities in the ground state.
Later I believe this statement is refined to reduction in the bond order, because of or leading to lengthening of the double bond, which reduces steric hindrance and allows rotation.

Using similar methods to the more recent paper, this paper uses B3LYP with 6-31G* and PM3 to calculate the ground state potential energy surface of a Feringa-type molecular motor.
The two helicities differ by about 3 kcal/mol but are separated by a large barrier, around 22 kcal/mol here, governed by the overcrowded alkene. This transition state was found using a QM search method.
They also modeled the photoisomerization step and the excited state using spin-restricted ensemble-referenced Kohn-Sham (REKS) and time-dependent DFT, in a way that I don’t understand at all -- but they were able to arrive at the following free energy diagram, which is a very helpful visualization!

![The ground and excited state potential energy surfaces calculated in [@N6pRFM85]. 1 eV = 23 kcal/mol. One curious note is that this drawing suggests the most stable state in the excited state is in neither P nor M helicity.](images/Kazaryan-2010-Scheme-3.png){#fig:Kazaryan width="5in"}

I wish I understood this paper better, because it seems to have a lot of useful pieces of information, including MD simulations.
But the terminology change from other Feringa papers coupled with the advanced QM methods make it difficult to penetrate. I should give it another go sometime.


### Commentary on reference 29 from [@xZIRNGMm] -- "Surface Hopping Excited-State Dynamics Study of the Photoisomerization of a Light-Driven Fluorene Molecular Rotary Motor" [@so4s7d25]
This paper purports to use design principles in the lowering of the energy barrier for rotation, thus speeding up the motor.
To reach the conical intersection CI (between the excited and ground states), the ground state needs to undergo geometric distortion, twisting the double bond, causing pyramidalization of the central carbon.
I’m not sure if the driving force for this is thermal or something else.
Instead of allowing the molecule to switch states based on how close it is to the CI, this reference uses semiclassical trajectory hopping simulations and on-the-fly QM calculations.
Ah yes, I remember reading this paper before.
It has the same first author (Kazaryan) and I find both of his papers difficult to follow.

### Mechanism of isomerization
These papers got me thinking about the exact mechanism underlying the cis/trans isomerization of the double bond.
[@isrZfXcg]
[@q3LAChQb]

## "Ultrafast dynamics"

## "Tuning the rotation rate"