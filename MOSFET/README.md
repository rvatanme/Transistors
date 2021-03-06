# Introduction
The metal-oxide-semiconductor field-effect transistor (MOSFET) is the most-important device for forefront high-density integrated circuits such as 
microprocessors and semiconductor memories. It is also becoming an important power device.

## Field-Effect Transistors: Family Tree
The MOSFET is the main member of the family of field-effect transistors. A distinction between the field-effect transistor (FET) and the potential-effect transistor (PET) is warranted here. A transistor in general is a three-terminal device where the channel resistance between two of the contacts is controlled by the third (MOSFETs have the fourth terminal as contact to the substrate). The difference between the FET and the PET is the way the control is coupled to the channel. As shown in the following figure, in an FET, the channel is controlled capacitively by an electric field (hence the name field-
effect), and in a PET, the channel’s potential is accessed directly (hence the name potentideffect). Conventionally in FETs, the channel carriers flow from the source to the drain, and the control terminal is called the gate, whereas in PETs, these corresponding terminals are called the emitter, collector, and base, respectively. The bipolar transistor is a good representative of the PETs.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/FET_PET.png)

A family tree of field-effect transistors is shown in the following The three first-level main members are IGFET (insulated-gate FET), JFET (junction FET), and MESFET (metal-semiconductor FET). They are distinguished by the way the gate capacitor is formed. In an IGFET, the gate capacitor is an insulator. In a JFET or a MESFET, the capacitor is formed by the depletion layer of a p-n junction or a Schottky barrier, respectively. In the branch of IGFET, we further divide it into MOSFET/MISFET (metal-insulator-semiconductor FET) and HFET (heterojunction FET). In the MOSFET, specifically the insulator is a grown oxide layer, whereas in the MISFET the insulator is a deposited dielectric. In the HFET branch, the gate material is a high-bandgap semiconductor layer grown as a heterojunction which acts as an insulator.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/FET_Family.png)

There are many ways to categorize the versions of FETs. First, according to the type of channel carriers, we have n-channel andp-channel devices. n-channels are formed by electrons and are more conductive with more positive gate bias, whilep-channels are formed by holes and are more conductive with more negative gate bias. Furthermore, it is important to describe the state of the transistor with zero gate bias. FETs are called enhancement-mode, or normally-off, if at zero gate bias the channel conductance is very low and we must apply a gate voltage to form a conductive channel. The counterpart is called depletion-mode, or normally-on, when the channel is conductive with zero gate bias and we must apply a gate voltage to turn the transistor off.

It is important also to point out the nature of the channel in more details. According to the following figure, a channel can be formed by a surface inversion layer or a bulk buried layer. The surface inversion channel is a two-dimensional charge sheet of thickness in the order of 5 nm. The buried channel is much thicker, comparable to the depletion width since when the transistor is turned off, the channel is totally con-
sumed by the surface depletion layer. In the FET family, MESFETs and JFETs are always buried-channel devices, while MODFETs are surface-channel devices.
MOSFETs and MISFETs can have both kinds of channels in parallel, but in practice, they are mostly surface-channel devices.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/channel.png)

These two kinds of channels offer advantages of their own. Buried channels are based on bulk conduction and, thus, are free of surface effects such as scattering and surface defects, resulting in better carrier mobility. On the other hand, the physical distance between the gate and the channel is larger and also dependent on gate bias, leading to a lower and variable transconductance. Note that for depletion-mode devices, it is common to use buried channels, but theoretically, one can achieve the same goal by choosing a gate material with a proper work function to shift the threshold voltage to a desirable value.

## Basic Device Characteristics
As shown in the following figure, the basic device parameters are the channel length L , which is the distance between the two metallurgical n+-p junctions; the channel width Z; the insulator thickness d; the junction depth r<sub>j</sub>; and the substrate doping NA. In a silicon integrated circuit, a MOSFET is surrounded by a thick oxide (called the field oxide to distinguish it from the gate oxide) or a trench filled with insulator to electrically isolate it from adjacent devices.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/MOSFET_Stru.png)

When a voltage is applied across the source-drain contacts, the MOS structure is in a nonequilibrium condition; that is, the minority-carrier (electron in the present case) quasi-Fermi level E<sub>Fn</sub>, is lowered from the equilibrium Fermi level. The two-dimensional, flat-band, zero-bias ( V<sub>G</sub> = V<sub>D</sub> = V<sub>BS</sub> = 0) equilibrium condition is shown in Fig. b. The equilibrium condition but under a gate bias that causes surface inversion is shown in Fig. c. The nonequilibrium condition with both drain and gate biases is shown in Fig. d, where we note the separation of the quasi-Fermi levels of electrons E<sub>Fn</sub>, and holes E<sub>Fp</sub>; the E<sub>Fp</sub> remains at the bulk Fermi level while E<sub>Fn</sub> is lowered toward the drain contact. Figure d shows that the gate voltage required for inversion at the drain is larger than the equilibrium case in which ψ<sub>s</sub>(inv) = 2ψ<sub>B</sub>.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/MOSFET_Band_diag.png)

The following figure shows a comparison of the charge distribution and energy-band variation of an inverted p-region for the equilibrium case and the nonequilibrium case at the drain. For the equilibrium case, the surface depletion region reaches a maximum width W<sub>Dm</sub> at inversion. For the nonequilibrium case, the depletion-layer width is deeper than WDm and is a function of the drain bias V<sub>D</sub>. The surface potential ψ<sub>s</sub>(inv) at the drain at the onset of strong inversion is, to a good approximation, given by ψ<sub>s</sub>(inv) = V<sub>D</sub> + 2ψ<sub>B</sub>.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Inv_Drain.png)

Since the concentration of carrier under non-equilibrium condition is govern by quasi-Fermi levels, two following assumptions are considered in order to derive the characteristics of the surface space charge; (1) the majority-carrier quasi-Fermi level E<sub>Fp</sub> is the same as that of the substrate and it does not vary with distance from the bulk to the surface (constant with x), and (2) the minority-carrier quasi-Fermi level E<sub>Fn</sub> is lowered by the drain bias by an amount dependent on the y-position. Based on these assumptions, the one-dimensional Poisson equation for the surface space-charge region at the drain end is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20p%3Dn_iexp%28%5Cfrac%7BE_i-E_%7BFp%7D%7D%7BkT%7D%29%20%5C%5C%5C%5C%20n%3Dn_iexp%28%5Cfrac%7BE_%7BFn%7D-E_i%7D%7BkT%7D%29)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bd%5E2%5Cpsi_p%7D%7Bdx%5E2%7D%20%3D%20%5Cfrac%7Bq%7D%7B%5Cepsilon_s%7D%28N_A-p&plus;n%29%20%5C%5C%5C%5C%20p%3DN_Aexp%28-%5Cbeta%20%5Cpsi_p%29%20%5C%5C%5C%5C%20n%3Dn_%7Bp0%7Dexp%28%5Cbeta%20%5Cpsi_p%20-%20%5Cbeta%20V_D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%20%5Cbeta%20%5Cequiv%20q/kT)

Conceptually the charge due to minority carriers within the inversion layer, is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%7C%20%3D%20q%5Cint_%7B0%7D%5E%7Bx_i%7Dn%28x%29dx%20%3D%20q%5Cint_%7B%5Cpsi_s%7D%5E%7B%5Cpsi_B%7D%20%5Cfrac%7Bn%28%5Cpsi_p%29d%5Cpsi_p%7D%7Bd%5Cpsi_p/dx%7D%20%5C%5C%5C%5C%5C%5C%20q%5Cint_%7B%5Cpsi_s%7D%5E%7B%5Cpsi_p%7D%5Cfrac%7Bn_%7Bp0%7Dexp%28%5Cbeta%5Cpsi_p-%5Cbeta%20V_D%29d%5Cpsi_p%7D%7B%28%5Csqrt2kT/qL_D%29F%28%5Cbeta%5Cpsi_p%2CV_D%2Cn_%7Bp0%7D/p_%7Bp0%7D%29%7D%20%5C%5C%5C%5C%5C%5C%20F%28%5Cbeta%5Cpsi_p%2CV_D%2Cn_%7Bp0%7D/p_%7Bp0%7D%29%5Cequiv%20%5C%5C%5C%5C%20%5Csqrt%7Bexp%28-%5Cbeta%5Cpsi_p%29&plus;%5Cbeta%5Cpsi_p-1&plus;%5Cfrac%7Bn_%7Bp0%7D%7D%7Bp_%7Bp0%7D%7Dexp%28-%5Cbeta%20V_D%29%5Bexp%28%5Cbeta%5Cpsi_p%29-%5Cbeta%5Cpsi_pexp%28%5Cbeta%20V_D%29&plus;1%5D%7D)

where x<sub>i</sub> denotes the point at which qψ<sub>p</sub>(x) = E<sub>Fn</sub> - E<sub>i</sub>(x) = qψ<sub>B</sub>. For the practical doping ranges in silicon, the value of x, is quite small, of the order of 3 to 30 nm. The above equation is the exact formulation, but can only be evaluated numerically. To get an analytical solution we follow the same approach as in MOS analysis. The surface electric field in the x-direction at the drain end is given by: 

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cxi_s%3D-%5Cfrac%7Bd%5Cpsi_p%7D%7Bdx%7D%7C_%7Bx%3D0%7D%3D%5Cpm%20%5Cfrac%7B%5Csqrt2%20kT%7D%7BqL_D%7DF%28%5Cbeta%20%5Cpsi_s%2CV_D%2C%5Cfrac%7Bn_%7Bp0%7D%7D%7Bn_%7Bp0%7D%7D%29)

and the total semiconductor surface charge is then obtained from Gauss' law:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_s%3D%5Cepsilon_s%5Cxi_s%3D%5Cpm%20%5Cfrac%7B%5Csqrt2%20%5Cepsilon_skT%7D%7BqL_D%7DF%28%5Cbeta%20%5Cpsi_s%2CV_D%2C%5Cfrac%7Bn_%7Bp0%7D%7D%7Bn_%7Bp0%7D%7D%29%20%5C%5C%5C%5C%20L_D%5Cequiv%20%5Csqrt%7B%5Cfrac%7BkT%5Cepsilon_s%7D%7BN_Aq%5E2%7D%7D)

where L<sub>D</sub> is the Debye length. The inversion charge per unit area Q<sub>n</sub> after strong inversion is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_n%3DQ_s-Q_B)

where the depletion bulk charge is:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_B%3DqN_AW_D%3D%5Csqrt%7B2qN_A%5Cepsilon_s%28V_D&plus;2%5Cpsi_B%29%7D)

After some mathematical simplification, the inversion charge Q<sub>s</sub> at the drain end as a function of surface potential can be given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%7C%3D%5Csqrt2qN_AL_D%5B%5Csqrt%7B%5Cbeta%5Cpsi_s&plus;%5Cfrac%7Bn_%7Bp0%7D%7D%7Bp_%7Bp0%7D%7Dexp%28%5Cbeta%5Cpsi_s-%5Cbeta%20V_D%29%7D&plus;%5Csqrt%7B%5Cbeta%5Cpsi_s%7D%5D)

This solution is still difficult to use because at strong inversion, Q<sub>s</sub> is very sensitive to the surface potential. Another shortcoming is that
the relationship to the terminal bias, that is V<sub>G</sub>, is still missing. The charge-sheet model discussed in the following section is simpler and much more useful for deriving the I-V characteristics of MOSFETs.

### Charge-Sheet Model
In the charge-sheet model, under strong-inversion conditions, the inversion layer is treated as a charge sheet with zero thickness (xi = 0). Consequently, this assumption implies that the potential drop across this charge sheet is also zero. These assumptions do introduce error but within an acceptable level. From Gauss’s law, the boundary conditions on both sides of the charge sheet are:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cxi_%7Box%7D%5Cepsilon_%7Box%7D%20%3D%20%5Cxi_s%5Cepsilon_s%20-%20Q_n%20%5C%5C%5C%5C%20%5Cpsi_s%28y%29%20%5Capprox%20%5CDelta%5Cpsi_i%28y%29%20&plus;%202%5Cpsi_B%20%5C%5C%5C%5C%20%5CDelta%5Cpsi_i%28y%29%20%3D%20%5Cfrac%7BE_i%28x%3D0%2Cy%3D0%29-E_i%28x%3D0%2Cy%29%7D%7Bq%7D)

where Δψ<sub>i</sub>, is the channel potential with respect to the source end and is equal to V<sub>D</sub> at the drain end. Note that the electric fields
can be expressed as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cxi_%7Box%7D%20%3D%20%5Cfrac%7BV_G-%5Cpsi_s%7D%7Bd%7D%20%3D%20%5Cfrac%7BV_G-%28%5CDelta%5Cpsi_i&plus;2%5Cpsi_B%29%7D%7Bd%7D%20%5C%5C%5C%5C%20%5Cxi_%7Bs%7D%20%3D%20%5Csqrt%7B%5Cfrac%7B2qN_A%28%5CDelta%5Cpsi_i&plus;2%5Cpsi_B%29%7D%7B%5Cepsilon_s%7D%7D)

where an ideal MOS system with zero work-function difference is assumed. The semiconductor field is simply the maximum field at the edge of the depletion region. combining the above equation gives Qs in the following form:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%28y%29%7C%20%3D%20%5BV_G-%28%5CDelta%5Cpsi_i%28y%29&plus;2%5Cpsi_B%29%5DC_%7Box%7D-%20%5Csqrt%7B2%5Cepsilon_sqN_A%28%5CDelta%5Cpsi_i%28y%29&plus;2%5Cpsi_B%29%7D)

This final form will be used as the channel charge responsible for the current conduction.

## Current-Voltage Characteristics
For deriving the basic MOSFET I-V characteristics, we assume 1) there are no interface traps and mobile oxide charge in the gate structure 2) only drift current exists 3) doping in the chanel is uniform 4) reverse leakage current is negligable 5) the transverse field (field in the x-direction) is much larger than longitudinal field (field in the y-direction). This last condition corresponds to the so-called gradual-channel approximation. Note that in
condition 1 , the requirements of zero fixed oxide charge and work-function difference are removed, and their effects are included in a flat-band voltage V<sub>FB</sub> required by the gate to produce the flat-band condition. Consequently V<sub>G</sub> is replaced by V<sub>G</sub> - V<sub>FB</sub> for the inversion charge, giving:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_n%28y%29%3D%5BV_G-V_%7BFB%7D-%5CDelta%20%5Cpsi_i%28y%29-2%5Cpsi_b%5DC_%7Box%7D%20%5C%5C%5C%5C%20-%5Csqrt%7B2%5Cepsilon_sqN_A%5B%5CDelta%20%5Cpsi_i%28y%29&plus;2%5Cpsi_b%20%5D%7D)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%28y%29%20%3D%20Z%7CQ_n%28y%29%7C%5Cnu%28y%29%20%5C%3B%5C%3B%5C%3B%5C%3B%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7D%7CQ_n%28y%29%7C%5Cnu%28y%29dy)

where ν(y) is the average carrier velocity. The carrier velocity ν(y) is a function of the y-position since the longitudinal field χ<sub>y</sub>(y) is a variable. Because of this, the relationship between ν(y) and χ<sub>y</sub>(y) is important to evaluate the above equation. We first consider the case where χ<sub>y</sub>(y) is low such that the mobility is constant (for shorter channel lengths, higher field causes velocity saturation and ultimately ballistic transport). Under this assumption, the above equation is simplified to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%3D%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%5C%7B%20%28V_G-V_%7BFB%7D-2%5Cpsi_B-%5Cfrac%7BV_D%7D%7B2%7D%29V_D%20%5C%5C%5C%5C%20-%5Cfrac%7B2%7D%7B3%7D%5Cfrac%7B%5Csqrt%7B2%5Cepsilon_sqN_A%7D%7D%7BC_%7Box%7D%7D%5B%28V_D&plus;2%5Cpsi_B%29%5E%7B3/2%7D-%282%5Cpsi_B%29%5E%7B3/2%7D%5D%5C%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%282%29)

The above equation predicts that for a given V, the drain current first increases linearly with drain voltage (the linear region), then gradually levels off (the nonlinear region), and finally approaching a saturated value (the saturation region). A qualitative discussion of the device operation can be helpful, with the aid of the following Fig. 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/MOSFET_Operated.png)

Let us consider that a positive voltage is applied to the gate, large enough to cause an inversion at the semiconductor surface. If a small drain voltage is applied, a current will flow from the source to the drain through the conducting channel. The channel acts as a resistor, and the drain current I<sub>D</sub> is proportional to the drain voltage V<sub>D</sub>. This is the linear region. As the drain voltage increases, the current deviates from the linear relationship since the charge near the drain end is reduced by the channel potential Δψ<sub>i</sub>. It eventually reaches a point at which the inversion charge at the drain end Q<sub>n</sub>(L) is reduced to nearly zero. This location of Q<sub>n</sub> = 0 is called the pinch-off point. In reality Q<sub>n</sub>(L) is not zero for current continuity, but small because of its high field and high carrier velocity. Beyond this drain bias, the drain
current remains essentially the same, because for V<sub>D</sub> > V<sub>Dsat</sub>, the pinch-off point starts to move toward the source, but the voltage at this pinch-off point remains the same (V<sub>Dsat</sub>). Thus, the number of carriers arriving at the pinch-off point from the source, and hence the current, remains essentially the same, apart from a decrease in L to the value L' (Fig. c). This change of effective channel length will increase the drain current only when the shortened amount is a substantial fraction of the channel length. This will be considered in the section of short-channel effects.

We shall now consider the current equations for the three cases of linear, non-linear, and saturation regions. In the linear region, with a small V<sub>D</sub>, using power series around V<sub>D</sub> and taking only the initial terms, the above equation reduces to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%3D%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%5C%7B%20%28V_G-V_%7BFB%7D-2%5Cpsi_B-%5Cfrac%7BV_D%7D%7B2%7D%29V_D%20%5C%5C%5C%5C%20-%5Cfrac%7B2%7D%7B3%7D%5Cfrac%7B%5Csqrt%7B2%5Cepsilon_sqN_A%7D%7D%7BC_%7Box%7D%7D%5B%28V_D&plus;2%5Cpsi_B%29%5E%7B3/2%7D-%282%5Cpsi_B%29%5E%7B3/2%7D%5D%5C%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%282%29)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%3D%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%28V_G-V_T-%5Cfrac%7BV_D%7D%7B2%7D%29V_D%20%5C%5C%5C%5C%20for%20%5C%3B%5C%3B%5C%3B%5C%3B%20V_D%3C%3CV_G-V_T)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3D%20V_%7BFB%7D&plus;2%5Cpsi_B&plus;%5Cfrac%7B%5Csqrt%7B2%5Cepsilon_sqN_A%282%5Cpsi_B%29%7D%7D%7BC_%7Box%7D%7D)

where V<sub>T</sub> is the threshold voltage. 

The pinch-off point occurs because the relative voltage between the gate and the semiconductor is reduced. The drain voltage and the drain current at this point are designated as V<sub>Dsat</sub> and I<sub>Dsat</sub> respectively. Beyond the pinch-off point the current remains independent of V<sub>D</sub> and we have the saturation region. The value of V<sub>Dsat</sub> is obtained from Eq. 1 under the condition Q<sub>n</sub>(L) = 0. The solution yields:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BDsat%7D%20%3D%20%5CDelta%5Cpsi_i%28L%29%20%3D%20V_G%20-%20V_%7BFB%7D%20-%202%5Cpsi_B%20&plus;%20%5C%5C%5C%5C%20K%5E2%5B1-%5Csqrt%7B1&plus;%5Cfrac%7B2%28V_G-V_%7BFB%7D%29%7D%7BK%5E2%7D%7D%5D)

By Substituing V<sub>Dsat</sub> in the equation 2, the saturation current I<sub>Dsat</sub> is obtained as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZ%7D%7B2ML%7D%5Cmu_nC_%7Box%7D%28V_G-V_T%29%5E2%20%5C%5C%5C%5C%20M%5Cequiv%201&plus;%5Cfrac%7BK%7D%7B2%5Csqrt%7B%5Cpsi_B%7D%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20K%20%5Cequiv%20%5Cfrac%7B%5Csqrt%7B%5Cepsilon_sqN_A%7D%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BDsat%7D%20%3D%20%5Cfrac%7BV_G-V_T%7D%7BM%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%283%29)

M has a value slightly larger than unity and it approaches unity with thinner oxide and lower doping. Furthermore, a more convenient form for V<sub>Dsat</sub> can be expressed as above. The transconductance in the saturation region is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20%5Cfrac%7BdI_D%7D%7BdV_G%7D%7C_%7BV_D%20%3E%20V_%7BDsat%7D%7D%20%3D%20%5Cfrac%7BZ%7D%7BML%7D%5Cmu_nC_%7Box%7D%28V_G-V_T%29)

It can be seen here that in this saturation region, for constant mobility, the current is a square-law function according to Eq. 3, indicated by the increasing current steps between gate bias.

Finally, the nonlinear region in between these two extreme cases can be described well by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%28V_G-V_T-%5Cfrac%7BMV_D%7D%7B2%7D%29V_D)

Equation 1 for the inversion charge is an exact expression. An approximation of the following form, taking advantage of the definition of threshold voltage, can be made:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%28y%29%7C%20%3D%20C_%7Box%7D%28V_G-V_T-M%5CDelta%5Cpsi_i%28y%29%29)

This simplified charge expression is helpful to analyze the conditions under field-dependent mobility and velocity saturation which is discussed next.

### Velocity-Field Relationship
As technology advances and pushes for device performance and density, the channel length gets shorter and shorter. The internal longitudinal field ξ<sub>y</sub> in the channel also increases as a result. For low fields, the mobility is constant. This low-field mobility is used for the long-channel characteristics in the last section. In the extreme case of very high field, the velocity approaches a value, saturation velocity ν<sub>s</sub>. In between the constant-mobility regime and the saturation-velocity regime, the carrier velocity can be described by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cnu%28%5Cxi%29%20%3D%20%5Cfrac%7B%5Cmu%5Cxi%7D%7B%5B1&plus;%28%5Cmu%5Cxi/%5Cnu_s%29%5En%5D%5E%7B1/n%7D%7D%20%3D%20%5Cfrac%7B%5Cmu%5Cxi%7D%7B%5B1&plus;%28%5Cxi/%5Cxi_c%29%5En%5D%5E%7B1/n%7D%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%284%29)

where μ is the low-field mobility. The value of n changes the shape of the curve, but μ, ν<sub>s</sub>, and the critical field ξ<sub>c</sub> (= ν<sub>s</sub>/μ) remain the same. It has been observed that in silicon for electrons n = 2 and for holes n = 1 have the best fit. The value of ν<sub>s</sub> for electron in silicon at room temperature is around 1E7 cm/s. As the terminal voltage VD is increased from zero, current is increased because of higher field and higher velocity. Eventually the velocity reaches the maximum value of ν<sub>s</sub>, and the current also saturates to a constant value. Notice that this current saturation comes from a completely different mechanism than in the case of constant mobility. Here, it is due to velocity saturation of carriers, before the pinch-off condition can occur.

To derive the I-V characteristics it is important to know the ν-ξ relationship (the following figure). We find that mathematically, for Eq. 4 with n=2, the analysis is rather complicated. Fortunately for the cases of two-piece linear approximation (following figure) and the above equation with n=1, the mathematics is manageable and simple solutions can be obtained. Since these two extremes mostly cover the realistic bounds for different kinds of carriers, we will consider both assumptions.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/nu_xi_rela.png)

#### Field-Dependent Mobility: Two-Piece Linear Approximation
In the two-piece linear approximation, the constant-mobility model is valid up to the point when the maximum field near the drain exceeds ξ<sub>c</sub>. Conversely, Eq. 2 is valid up to a new V<sub>Dsat</sub> value which occurs earlier than the constant-mobility model, so the only task is to find the new V<sub>Dsat</sub> which is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%28y%29%7C%20%3D%20C_%7Box%7D%28V_G-V_T-M%5CDelta%5Cpsi_i%28y%29%29)


![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%28y%29%3DZ%7CQ_n%28y%29%7C%5Cnu%28y%29)


![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%28y%29%3DZC_%7Box%7D%5Cmu_n%5Cxi%20%28V_G-V_T-M%5CDelta%20%5Cpsi_i%29%20%5C%5C%5C%5C%20I_%7BDsat%7D%3DZC_%7Box%7D%5Cmu_n%5Cxi_c%20%28V_G-V_T-M%5CDelta%20V_%7BDsat%7D%29)

Here we need one more equation to solve for two unknowns. Using the following equations, we obtain an expression similar to linear region of IV curve given as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%28y%29%7C%20%3D%20C_%7Box%7D%28V_G-V_T-M%5CDelta%5Cpsi_i%28y%29%29)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%3D%5Cfrac%7BZ%7D%7BL%7D%5Cint_0%5EL%7CQ_n%28y%29%7C%5Cnu%28y%29dy)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%3D%5Cfrac%7BZC_%7Box%7D%5Cmu_n%7D%7BL%7D%28V_G-V_T-%5Cfrac%7BMV_%7BDsat%7D%7D%7B2%7D%29V_%7BDsat%7D)

By solving for V<sub>Dsat</sub>, we get:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BDsat%7D%20%3D%20L%5Cxi_c%20&plus;%20%5Cfrac%7BV_G-V_T%7D%7BM%7D%20-%20%5Csqrt%7B%28L%5Cxi_c%29%5E2%20&plus;%20%28%5Cfrac%7BV_G-V_T%7D%7BM%7D%29%5E2%7D%20%5C%5C%5C%5C%5C%5C%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZC_%7Box%7D%5Cmu_n%7D%7BL%7D%28V_G-V_T-%5Cfrac%7BMV_%7BDsat%7D%7D%7B2%7D%29V_%7BDsat%7D)

Since V<sub>Dsat</sub> here is always smaller than (V<sub>G</sub> - V<sub>T</sub>)/M, the field-dependent mobility always gives a lower I<sub>Dsat</sub>.

#### Field-Dependent Mobility: Empirical Formula 
Next we consider the ν-ξ relationship of Eq. 4 with n = 1. Substituting this into I<sub>D</sub> integral equation gives:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BD%7D%20%3D%20%5Cfrac%7BZC_%7Box%7D%5Cmu_n%5Cxi_c%7D%7BL%5Cxi_c&plus;V_D%7D%28V_G-V_T-%5Cfrac%7BMV_%7BD%7D%7D%7B2%7D%29V_%7BD%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BDsat%7D%20%3D%20L%5Cxi_c%5B%5Csqrt%7B1&plus;%5Cfrac%7B2%28V_G-V_T%29%7D%7BML%5Cxi_c%7D%7D-1%5D)

V<sub>Dsat</sub>, has been obtained by setting dI/dV = 0. Again, once V<sub>Dsat</sub> is known, I<sub>Dsat</sub>, can be calculated from the above equation. 

#### Velocity Saturation. 
Using either assumption described above, it is interesting and insightful to look at the extreme case of short-channel devices where velocity saturation completely limits the current flow. In such case we set ν = ν<sub>s</sub>, and consequently Q<sub>n</sub> has to be fixed for current continuity, and is approximated to be (VG - VT)Cox. Then ID integrand equation becomes:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7D%7CQ_n%28y%29%7C%5Cnu%28y%29dy%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%7CQ_n%7C%5Cnu_sL%20%5C%5C%5C%5C%5C%5C%20%3DZ%28V_G-V_T%29C_%7Box%7D%5Cnu_s%20%5C%5C%5C%5C%20g_m%5Cequiv%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20ZC_%7Box%7D%5Cnu_s)

To compare models based on constant mobility and velocity saturation, we show I-V curves of identical devices in the following figure. Several observations can be made. First, IDSat and VDSat are both lowered by velocity saturation, while the linear regions remain similar. The gm (which is the current difference between VG steps) also becomes a constant, independent of VG. Finally the above equation shows an interesting phenomena that the saturation current no longer depends on the channel length.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Mob_I_V.png)

Experimental data confirm that such simple theory is quite satisfactory. In reality, as above Fig indicates, the carrier velocity never reaches exactly us. Also the lateral field is not uniform throughout the channel. It is more difficult for the lower field near the source to reach ξ<sub>c</sub> and that presents a bottle-neck for the maximum current. A better agreement can often be reached by adding a pre-factor with a value of = 0.5-1.0 for the above equations.

In ultra-short channel lengths whose dimensions are on the order of or shorter than the mean free path, channel carriers do not suffer from scattering. They can gain energy from the field without losing it to the lattice through scattering, and can acquire a velocity much higher than the saturation velocity. This effect is called ballistic transport (or velocity overshoot by some). Computer simulations show that in these devices, the field and velocity are very nonuniform (shown in the following figure). Notice that the longitudinal field along the channel (dEC/dy) varies monotonically, being the highest at the drain end. Ballisticity always starts at the drain end, where the velocity can exceed the value of saturation velocity ν<sub>s</sub>. (For silicon at room temperature, ν<sub>s</sub> = ν<sub>th</sub>, the thermal velocity.) At positions closer to the source, the velocity decreases. In order to
have current continuity, the channel potential and inversion charge must adjust themselves such that the product of velocity and charge would remain constant throughout the channel. By such argument, the bottleneck for the current flow, at the extreme of ultra-short channel length, would be at the position of maximum charge and minimum field, which means the potential maximum near the source end, indicated in the Fig. a.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Ballestic.png)

In analyzing the saturation current in the ballistic regime, we go back to the general equation of ID integrand equation, and apply it to this maximum-potential point. We start with the generalized form I<sub>Dsat</sub> = Z|Q<sub>n</sub>|ν<sub>eff</sub>. where |Q<sub>n</sub>| has the maximum value at the source as Cox( VG - VT), and ν<sub>eff</sub> is an effective average carrier velocity that should match the final experimental saturation current. So in this simple expression, the only critical parameter is ν<sub>eff</sub>. 

The maximum value of ν<sub>eff</sub> according to classical thermal equilibrium, is simply the thermal velocity ν<sub>th</sub> [= (2kT/πm*)<sup>1/2</sup>]. Close examination of the system reveals that for higher inversion charge density, the random velocity can exceed this thermal limit. This is a quantum-mechanical effect, called carrier degenracy, where the mean carrier energy is pushed to a higher state than the thermal energy. This higher value is called the injection velocity ν<sub>inj</sub>, related to the Fermi energy with respect to the quantized energy En inside the potential well where carriers reside, under high inversion charge, given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cnu_%7Binj%7D%20%3D%20%5Cfrac%7B8%5Chbar%7D%7B3m%5E*%7D%5Csqrt%7B%5Cfrac%7B%7CQ_n%7C%7D%7B2%5Cpi%20q%7D%7D%20%3D%20%5Cfrac%7B8%5Chbar%7D%7B3m%5E*%7D%5Csqrt%7B%5Cfrac%7B%28V_G-V_T%29C_%7Box%7D%7D%7B2%5Cpi%20q%7D%7D)

Note that with a small inversion charge ν<sub>inj</sub> = ν<sub>th</sub>. Theoretical vinj as a function of the inversion charge is shown in the following figure. The maximum current, which is a product of Q<sub>n</sub>ν<sub>inj</sub>, gives the ultimate current drive of the ballistic MOSFET and is also plotted in the same figure.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/vinj_inver.png)

The saturation current of the above equation can be rewritten as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20%5Cfrac%7B8r_nZ%5Chbar%7D%7B3m%5E*%7D%7B%5Cfrac%7B%5B%28V_G-V_T%29C_%7Box%7D%5D%5E%7B3/2%7D%7D%7B%5Csqrt%7B2%5Cpi%20q%7D%7D%7D)

where r<sub>n</sub> is the index of ballisticity (= ν<sub>eff</sub>/ν<sub>inj</sub>). In the extreme of ballistic transport, r<sub>n</sub> = 1, and it sets the ultimate current drive for L -> 0. The transconductance is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20%5Cfrac%7B4r_n%5Chbar%7D%7Bm%5E*%7D%5Csqrt%7B%5Cfrac%7B%28V_G-V_T%29C_%7Box%7D%7D%7B2%5Cpi%20q%7D%7D)

It is seen here that both IDsat and gm are independent of channel length L. The index of ballisticity is also interpreted by back scattering R of channel carriers at the drain back to the source. Furthermore, since mobility is also a consequence of scattering, there should be some relationship between r<sub>n</sub> and the low-field mobility μ<sub>n</sub>. It has been shown that:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20r_n%20%3D%20%5Cfrac%7B%5Cnu_%7Beff%7D%7D%7B%5Cnu_%7Binj%7D%7D%20%3D%20%5Cfrac%7B1-R%7D%7B1&plus;R%7D%20%5C%5C%5C%5C%20%3D%20%5B%5Cfrac%7B1%7D%7B%5Cnu_%7Binj%7D%7D&plus;%5Cfrac%7B1%7D%7B%5Cmu_n%5Cxi%280%5E&plus;%29%7D%5D%5E%7B-1%7D)

where ξ(0+) is the field at a potential kT down from the maximum toward the drain. It should be emphasized that in this model, at or near the maximum-potential point, the field is too low to cause ballistic transport, so ν<sub>inj</sub> sets the maximum current, even though a location near the drain can have ballistic transport. The high ballistic velocities near the drain cannot produce a higher current than vinj can support, but it helps to achieve this maximum value set by ν<sub>inj</sub> by rebalancing the whole system.
It is interesting to compare the VG dependence of IDsat for different channel lengths. In the long-channel, constant-mobility regime, IDsat ∝ (VG - VT)^2. In the short-channel, saturation-velocity regime, IDsat ∝ (VG - VT). And in the limit of ballistic regime, IDsat ∝ (VG - VT)^3/2.

To account for the threshold shift from nonzero flat-band voltage whose main cause comes from fixed oxide charges Q<sub>inj</sub> and the work-hnction difference φ<sub>ms</sub> between the gate material and the semiconductor, we get:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3DV_%7BFB%7D&plus;2%5Cpsi_B&plus;%5Cfrac%7B%5Csqrt%7B2qN_A%5Cepsilon_s%282%5Cpsi_B%29%7D%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%20%3D%20%28%5Cphi_%7Bms%7D%20-%20%5Cfrac%7BQ_f%7D%7BC_%7Box%7D%7D%29&plus;2%5Cpsi_B&plus;%5Cfrac%7B%5Csqrt%7B2qN_A%5Cepsilon_s%282%5Cpsi_B%29%7D%7D%7BC_%7Box%7D%7D)

Qualitatively, VT is the gate bias beyond flat-band just starting to induce an inversion charge sheet and is given by the sum of voltages across the semiconductor (2ψ<sub>B</sub>) and the oxide layer. The square-root term is the total depletion-layer charge. When a substrate bias is applied (negative for n-channel or p-substrate), the threshold voltage becomes:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3DV_%7BFB%7D&plus;2%5Cpsi_B&plus;%5Cfrac%7B%5Csqrt%7B2qN_A%5Cepsilon_s%282%5Cpsi_B-V_%7BBS%7D%29%7D%7D%7BC_%7Box%7D%7D)

In practice it is often necessary to minimize the threshold-voltage shift due to substrate bias. In these cases, low substrate doping and thin oxide thickness are preferred. To measure the threshold voltage, we use the linear region by applying a small drain bias (VD << VG, and plot ID versus VG, the the intercept would be VT + VD/2. 

When the gate bias is below the threshold and the semiconductor surface is in weak inversion or depletion, the corresponding drain current is called the subthreshold current. The subthreshold region tells how sharply the current drops with gate bias and is particularly important for low-voltage, low-power applications, such as when the MOSFET is used as a switch in digital logic and memory applications. 

In weak inversion and depletion, the electron charge is small and, thus, the drift current is low. The drain current is dominated by diffusion and is derived in the same way as the collector current in a bipolar transistor with homogeneous base doping. Considering the electron-density gradient in the channel, the diffusion current is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20-%20ZqD_n%5Cfrac%7BdN%27%28y%29%7D%7Bdy%7D%20%5Capprox%20ZqD_n%5Cfrac%7BN%27%280%29-N%27%28L%29%7D%7BL%7D%20%5C%5C%5C%5C%5C%5C%20N%27%280%29%20%3D%20%5Cint_%7B0%7D%5E%7BW_D%7D%20n%28x%29dx%20%3D%20n_%7Bp0%7D%5Cint_%7B%5Cpsi_s%7D%5E%7B0%7Dexp%28%5Cbeta%5Cpsi_p%29d%5Cpsi_p%20%5C%5C%5C%5C%20%5Capprox%20%5Cfrac%7B1%7D%7B%5Cbeta%7D%5Csqrt%7B%5Cfrac%7B%5Cepsilon_s%7D%7B2qN_A%5Cpsi_s%7D%7Dn_%7Bp0%7Dexp%28%5Cbeta%5Cpsi_p%29)

where N' is the electron density per unit area, integrated over the depletion width. The electron density at the drain end is lowered exponentially by the drain bias:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20N%27%28L%29%20%3D%20N%27%280%29exp%28-%5Cbeta%20V_D%29)

By combining the above equations, the ID current is derived as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20%5Cfrac%7BZ%5Cmu_n%7D%7BL%5Cbeta%5E2%7D%5Csqrt%7B%5Cfrac%7BqN_A%5Cepsilon_s%7D%7B2%5Cpsi_s%7D%7Dn_%7Bp0%7Dexp%28%5Cbeta%20%5Cpsi_s%29)

when VD >> kT/q. The above Eq. indicates that in the subthreshold region the drain current varies exponentially with ψs, and for drain voltage VD larger than = 3kT/q, the current becomes independent of VD. Next, in order to relate current to the gate bias, the relationship between VG and ψs is needed. From Chapter 4 on the MOS capacitor, we have the following relationship:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_G-V_%7BFB%7D%20%3D%20%5Cpsi_s%20&plus;%20%5Cfrac%7B%5Csqrt%7B2qN_A%5Cepsilon_s%5Cpsi_s%7D%7D%7BC_%7Box%7D%7D)

This quadratic equation will not give a simple expression of ψs as a function of VG But once ψs is known from the abovr Eq., the subthreshold current can be calculated. The parameter to quantify how sharply the transistor is turned off by the gate voltage is called the subthreshold swing S (inverse of subthreshold slope), defined as the gate-voltage change needed to induce a drain-current change of one order of magnitude. First from the above equation, the relative change of VG and ψs is calculated to be:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7BdV_G%7D%7Bd%5Cpsi_s%7D%20%3D%201%20&plus;%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%5Csqrt%7B%5Cfrac%7B%7BqN_A%5Cepsilon_s%7D%7D%7B2%5Cpsi_s%7D%7D%3D%5Cfrac%7BC_%7Box%7D&plus;C_D%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%5C%5C%20S%20%3D%20ln%2810%29%5Cfrac%7BkT%7D%7Bq%7D%5Cfrac%7BC_%7Box%7D&plus;C_D%7D%7BC_%7Box%7D%7D)

In the presence of a significant interface-trap density Dit, its associated capacitance Cit (= q2Dit) is in parallel with the depletion-layer capacitance CD. Therefore:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20S%20%28with%5C%3BD_%7Bit%7D%29%3D%20ln%2810%29%5Cfrac%7BkT%7D%7Bq%7D%5Cfrac%7BC_%7Box%7D&plus;C_D&plus;C_%7Bit%7D%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%5C%5C%20%3DS%28without%5C%3BD_%7Bit%7D%29%5Cfrac%7BC_%7Box%7D&plus;C_D&plus;C_%7Bit%7D%7D%7BC_%7Box%7D&plus;C_D%7D)

If other device parameters such as doping and oxide thickness are known, by measuring the subthreshold swing, the interface-trap density can be obtained. This provides an attractive option in measuring Di, besides using the MOS capacitor in which ac measurements have to be made. In general, dc I-Vmeasurements are much easier to make than ac capacitance and conductance, provided a three-terminal transistor structure is available (substrate contact is not critical here).

For a sharp subthreshold slope (small S), it is preferable to have low channel doping, thin oxide thickness, low interface-trap density, and low-temperature operation. When a substrate bias is applied, in addition to shifting the threshold voltage, it increases the value of ψs by VBS Consequently, the depletion-layer capacitance CD is reduced and therefore S is reduced.

At and near the threshold voltage, the drain current does not turn off as sharply as the equation predicts. This is due to diffhion current which is the dominant current near and below threshold, and it has been ignored so far, as one of the assumptions made at the beginning of the Section. To consider the effect of the difision component, we refer to Fig. 7 for the nonequilibrium condition. The total drain current density including both drift and difision components is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20J_D%28x%2Cy%29%20%3D%20qn%5Cmu_n%5Cxi_y&plus;qD_n%5Cfrac%7Bdn%7D%7Bdy%7D%20%3D%20D_nn%28x%2Cy%29%5Cfrac%7BdE_%7BFn%7D%7D%7Bdy%7D)

The drain current based on the gradual-channel approximation is:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3DZ%20%5Cint_%7B0%7D%5E%7Bx_i%7DJ_D%28x%2Cy%29dy%20%3D%20%5Cfrac%7BZD_n%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7D%5Cfrac%7BdE_%7BFn%7D%7D%7Bdy%7D%5Cint_%7B0%7D%5E%7Bx_i%7Dn%28x%2Cy%29dxdy%20%5C%5C%5C%5C%5C%5C%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cfrac%7B%5Cmu_n%5Cepsilon_s%7D%7BL_D%7D%5Cint_%7B0%7D%5E%7BV_D%7D%5Cint_%7B%5Cpsi_B%7D%5E%7B%5Cpsi_s%7D%5Cfrac%7Bexp%28%5Cbeta%5Cpsi_p-%5Cbeta%5CDelta%5Cpsi_i%29%7D%7BF%28%5Cbeta%5Cpsi_p%2C%5CDelta%5Cpsi_i%2Cn_%7Bp0%7D/p_%7Bp0%7D%29%7Dd%5Cpsi_pd%5CDelta%5Cpsi_i)

The gate voltage VG is related to the surface potential ψs by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_G-V_%7BFB%7D%20%3D%20-%5Cfrac%7BQ_s%7D%7BC_%7Box%7D%7D&plus;%5Cpsi_s%20%5C%5C%5C%5C%20%3D%5Cfrac%7B2%5Cepsilon_skT%7D%7BC_%7Box%7DqL_D%7DF%28%5Cbeta%5Cpsi_p%2C%5CDelta%5Cpsi_i%2Cn_%7Bp0%7D/p_%7Bp0%7D%29&plus;%5Cpsi_s)

For a particular device with known physical dimensions and other device parameters, above equations can be calculated numerically to give accurate results for the entire range of drain voltage, from the linear region to the saturation region.

Because channel carriers are confined to a thin inversion layer, their drift velocity υ and mobility μ are expected to be influenced by the thickness of this inversion layer. Experimental measurements on Si inversion layers show that this low-field mobility, while independent of ξ<sub>y</sub> is a unique function of the transverse field ξ<sub>x</sub> that is perpendicular to the current. This dependence is not directly on the oxide thickness or doping density, but through their impact of ξ<sub>x</sub> in the inversion layer. The mobility is found to correlate well with a single parameter that is related to gX. At a given temperature, mobility decreases with an increasing effective transverse field, defined as the field averaged over the electron distribution in the inversion layer, given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%28%5Cxi_x%29_%7Beff%7D%20%3D%20%5Cfrac%7B1%7D%7B%5Cepsilon_s%7D%28Q_B&plus;%5Cfrac%7BQ_n%7D%7B2%7D%29)

Physically it means an average inversion carrier experiences the fill effect of the depletion-layer charge Q<sub>B</sub> but only half of the inversion-layer charge Q<sub>n</sub>.

Temperature affects device parameters and performance, in particular mobility, threshold voltage, and subthreshold characteristics. The effective mobility in inversion layer has a T<sup>-2</sup> power dependence on temperatures around 300 K at gate biases corresponding to strong inversion. This gives rise to higher current and transconductance at lower temperature.

To derive the temperature dependence of the threshold voltage, we repeat the following expression:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3D%20%28%5Cphi_%7Bms%7D%20-%20%5Cfrac%7BQ_f%7D%7BC_%7Box%7D%7D%29&plus;2%5Cpsi_B&plus;%5Cfrac%7B%5Csqrt%7B2qN_A%5Cepsilon_s%282%5Cpsi_B%29%7D%7D%7BC_%7Box%7D%7D)

Because the work-function difference φ<sub>ms</sub> and the fixed oxide charges are essentially independent of temperature, differentiating the above equation with respect to temperature yields:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7BdV_T%7D%7BdT%7D%20%3D%20%5Cfrac%7Bd%5Cpsi_B%7D%7BdT%7D%282&plus;%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%5Csqrt%7B%5Cfrac%7B%5Cepsilon_sqN_A%7D%7B%5Cpsi_B%7D%7D%29%20%5C%5C%5C%5C%5C%5C%20%5Cpsi_B%20%3D%20%5Cfrac%7BkT%7D%7Bq%7Dln%28%5Cfrac%7BN_A%7D%7Bn_i%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20n_i%5E2%20%5Cpropto%20T%5E3exp%28%5Cfrac%7B-E_%7Bg0%7D%7D%7BkT%7D%29%20%5C%5C%5C%5C%5C%5C%20%5Cfrac%7Bd%5Cpsi_B%7D%7BdT%7D%20%5Capprox%20%5Cfrac%7B1%7D%7BT%7D%28%5Cpsi_B-%5Cfrac%7BE_%7Bg0%7D%7D%7B2q%7D%29)

The following figure shows the results of such calculations at room temperature as a function of substrate doping for various values of oxide thickness. Note that depending on the oxide thickness, the quantity dVT/dT can increase or decrease with the substrate doping.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Thereshold_temp.png)

As temperature decreases, the MOSFET characteristics improve, especially in the subthreshold region. The most-important improvement is the reduction of the subthreshold swing S, from 80 mV/decade at 296 K to 22 mV/decade at 77 K. Thus, the improvement in the subthreshold swing at 77 K is about a factor of four. This improvement comes mainly from the kT/q term in Eq. 60. Other improvements at 77 K include higher mobility, thus, higher current and transconductance, lower power consumption, lower junction leakage current, and lower metalline resistance. The major disadvantages are that the MOSFET must be immersed in a suitable inert coolant (e.g., liquid nitrogen), and that a low-temperature setup requires additional equipment and special care.

## NOnuniform Doping and Buried-Channel Device
So far, doping concentration in the channel is assumed to be constant. In practical devices, however, the doping is generally nonuniform because in modern
MOSFET technology, ion implantation is used extensively to taylor the doping profile and improve the device performance for specific applications. For example, a lighter doping at deeper region reduces drain-substrate capacitance and also the substrate-bias effect. On the other hand, a lighter doping level near the Si-SiO2 interface lowers the threshold voltage, reduces the field and improves mobility, and higher level at deeper region reduces punch-through between source and drain. These two general cases, namely highilow and low-high profiles, shown in the following figure, with their step-profile approximations for ease of analysis.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Doping_profile.png)

### High-Low Profile: 
We consider next the effect of nonuniform channel doping on device characteristics, especially on threshold voltage and depletion width which in turn affects subthreshold swing and the substrate-bias effect. Note that what is most important for determining VT is the doping profile within the depletion region. The profile outside the depletion is important for considerations of capacitance and substrate sensitivity, that is, dependence of the threshold voltage on the substrate reverse bias. With that in mind, the general equation for the threshold voltage is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3D%20V_%7BFB%7D%20&plus;%20%5Cpsi_s%20&plus;%20%5Cfrac%7BQ_n%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%20%3D%20V_%7BFB%7D%20&plus;%202%5Cpsi_B%20&plus;%20%5Cfrac%7Bq%7D%7BC_%7Box%7D%7D%5Cint_%7B0%7D%5E%7BW_%7BDm%7D%7DN%28x%29dx%20%5C%3B%5C%3B%5C%3B%5C%3B%20%284%29%20%5C%5C%5C%5C%5C%5C%20%5Cpsi_s%20%3D%202%5Cpsi_B%20%3D%20%5Cfrac%7Bq%7D%7B%5Cepsilon_s%7D%5Cint_%7B0%7D%5E%7BW_%7BDm%7D%7DxN%28x%29dx%20%5C%3B%5C%3B%5C%3B%5C%3B%20%285%29)

The limit for integration, that is the maximum depletion width W<sub>Dm</sub> is needed and determined by the Poisson equation with the onset of strong inversion being the above boundary condition. Note that for a nonuniform profile, the definitions of ψ<sub>B</sub> and V<sub>FB</sub> become nontrivial and complicated. Fortunately, using the background doping of N<sub>B</sub> for these values is found to be sufficiently accurate.

To derive the threshold voltage shift due to ion implantation, we shall consider an idealized step profile as shown in the above Fig. The implant profile, after thermal anneal, is approximated by the step function with step depth x<sub>s</sub>, roughly equal to the sum of the projected range and the standard deviation of the original implant. For a wider x<sub>s</sub>, that is, the maximum depletion-layer width W<sub>Dm</sub>, under heavy inversion is within x<sub>s</sub>, the surface region can be considered a uniformly doped region with a higher concentration and the threshold voltage is calculated using the previously given equations. If Wx<sub>Dm</sub> > x<sub>s</sub> the threshold voltage is obtained from Eq. 4:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3D%20V_%7BFB%7D%20&plus;%202%5Cpsi_B%20&plus;%20%5Cfrac%7BqN_BW_%7BDm%7D&plus;q%5CDelta%20Nx_s%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%20%3D%20V_%7BFB%7D%20&plus;%202%5Cpsi_B%20&plus;%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%5Csqrt%7B2q%5Cepsilon_s%20N_B%282%5Cpsi_B-%5Cfrac%7Bq%5CDelta%20Nx%5E2%7D%7B2%5Cepsilon_s%7D%29%7D%20%5C%5C%5C%5C&plus;%20%5Cfrac%7Bq%5CDelta%20Nx_s%7D%7BC_%7Box%7D%7D)

The depletion width can be obtained from Eq. 5, using ψ<sub>s</sub> = 2ψ<sub>B</sub> for strong inversion:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20W_%7BDm%7D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_B%7D%282%5Cpsi_B-%5Cfrac%7Bq%5CDelta%20Nx%5E2%7D%7B2%5Cepsilon_s%7D%29%7D)

From these equations, we see that added surface doping increases V<sub>T</sub> and decreases W<sub>Dm</sub>. Notice that for the same dose, the V<sub>T</sub> shift is largest with the added doping closest to the surface. For the limiting case of a delta function of dose localized at the Si-SiO<sub>2</sub> interface (x<sub>s</sub> = 0), the threshold shift is simply qD<sub>I</sub>/C<sub>ox</sub>, where D<sub>I</sub> is the total dose ΔNx<sub>s</sub>. Such approach is called threshold adjust, which has the same effect as changing the work-function difference qφ<sub>ms</sub> or changing the total fixed oxide charge.

The step-profile approach described above can give first-order results for the threshold voltage. To obtain a more accurate V<sub>T</sub>, we have to consider the actual doping profile, because the step width x<sub>s</sub> is not well defined for nonuniform doping. A schematic diagram for the nonuniform implanted doping N(x) is shown in the following Fig. For a typical case, the threshold voltage depends on the implanted dose D<sub>I</sub> and the centroid of the dose x<sub>c</sub>. Therefore, the actual implant can be replaced by a delta-function located at x = x<sub>c</sub> as shown;

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Nonuniform_Doping.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20D_I%20%3D%20%5Cint_%7B0%7D%5E%7BW_%7BDm%7D%7D%5CDelta%20N%28x%29dx%20%5C%3B%5C%3B%5C%3B%5C%3B%20x_c%20%3D%20%5Cfrac%7B1%7D%7BD_I%7D%5Cint_%7B0%7D%5E%7BW_%7BDm%7D%7Dx%5CDelta%20N%28x%29dx%20%5C%5C%5C%5C%5C%5C%20V_T%20%3D%20V_%7BFB%7D%20&plus;%202%5Cpsi_B%20&plus;%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%5Csqrt%7B2q%5Cepsilon_s%20N_B%282%5Cpsi_B-%5Cfrac%7Bqx_cD_I%7D%7B%5Cepsilon_s%7D%29%7D%20%5C%5C%5C%5C%20&plus;%5Cfrac%7BqD_I%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%20W_%7BDm%7D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_B%7D%282%5Cpsi_B-%5Cfrac%7Bqx_cD_I%7D%7B%5Cepsilon_s%7D%29%7D)

It is interesting to examine the dependence of the threshold voltage shift and depletion width on the centroid x<sub>c</sub> for a given dose D<sub>I</sub>. As x<sub>c</sub> increases, the dose becomes less effective in changing V<sub>T</sub> and the depletion width W<sub>Dm</sub> decreases also at the same time. Eventually x<sub>c</sub> meets the depletion edge, and then W<sub>Dm</sub> becomes clamped to and increases with the implant centroid
x<sub>c</sub>. The condition for which x<sub>c</sub> starts to be equal to W<sub>Dm</sub> can be obtained as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20D_I%28x%3DW_%7BDm%7D%29%20%3D%20%5Cfrac%7BN_B%28W_%7BDm%7D%5E2-x_c%5E2%29%7D%7B2x_c%7D)

To consider the subthreshold swing and the substrate sensitivity, we have interpreted the subthreshold swing by comparing the gate-oxide capacitance
COX to depletion capacitance CD. So, once the depletion width is known, the subthreshold swing can be calculated. For the high-low profile, the added doping decreases WDm, increases CD, and results in a larger (less steep) subthreshold swing. The substrate sensitivity can be calculated also by substituting 2ψ<sub>B</sub> with 2ψ<sub>B</sub> + VBS in calculating VT.

### Low-High Profile:
Analysis of the low-high profile, also called the retrograde profile, is similar to the high-low case with a AN being subtracted from the background doping. The appropriate equations for the threshold voltage and depletion width become, with just a change of signs. The threshold voltage is, thus, decreased and the depletion width is increased by a dip at the surface doping.

## Buried-Channel Device
In the extreme case of the low-high profile, the surface doping can be of the opposite type of the substrate. When this happens, and if part of the surface doped layer is not fully depleted, that is, there exists some neutral region, current can conduct through this buried layer. We call this type of device a buried-channel device (shown in the following figure a). 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/burried_n_channel.png)

The gate voltage can change the surface depletion layer, thus controlling the net opening of the channel thickness and controlling the current flow. With a large positive gate bias, the channel is fully open, and an addition surface inversion layer can be induced at the surface, similar to a regular surface channel, resulting in two channels in parallel.

The net channel thickness is reduced from x<sub>s</sub> by the amounts of surface depletion W<sub>Ds</sub> and the bottom p-n junction depletion W<sub>Dn</sub>. The surface depletion as a function of V<sub>G</sub> is the same as Eq. 27 of Chapter 4, and is repeated and modified here as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20W_%7BDs%7D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_D%7D%28V_%7BFB%7D%5E*-V_G%29&plus;%5Cfrac%7B%5Cepsilon_s%5E2%7D%7BC_%7Box%7D%5E2%7D%7D-%5Cfrac%7B%5Cepsilon_s%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%20V_%7BFB%7D%5E*%20%3D%20V_%7BFB%7D&plus;%5Cpsi_%7Bbi%7D%20%5C%5C%5C%5C%20W_%7BDn%7D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%5Cpsi_%7Bbi%7D%7D%7BqN_D%7D%28%5Cfrac%7BN_A%7D%7BN_A&plus;N_D%7D%29%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%286%29)

Of special interest is the threshold voltage V<sub>T</sub> at which gate bias the channel width is totally consumed by both depletion regions. Setting the following condition, the threshold voltage is obtained as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20x_s%20%3D%20W_%7BDs%7D%20&plus;%20W_%7BDn%7D%20%5C%5C%5C%5C%20V_T%20%3D%20V_%7BFB%7D%5E*-qN_Dx_s%28%5Cfrac%7Bx_s%7D%7B2%5Cepsilon_s%7D&plus;%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%29&plus;%28%5Cfrac%7Bx_s%7D%7B%5Cepsilon_s%7D&plus;%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%29%5Csqrt%7B%5Cfrac%7B2q%5Cepsilon_sN_DN_A%5Cpsi_%7Bbi%7D%7D%7BN_A&plus;N_D%7D%7D%20%5C%5C%5C%5C%20-%5Cfrac%7BN_A%5Cpsi_%7Bbi%7D%7D%7BN_A&plus;N_D%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%287%29)

In the case of non-zero channel dimensions being known, the channel charge can be calculated easily. Depending on the gate-bias range, we can have different amounts of bulk change Q<sub>B</sub> and surface inversion charge Q<sub>I</sub>. These are given as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q%20%3D%20Q_B%20%3D%20%28x_s-W_%7BDs%7D-W_%7BDn%7D%29N_D%20%5C%5C%20for%20%5C%3B%5C%3B%5C%3B%20V_T%3CV_G%3CV_%7BFB%7D%5E*%20%5C%5C%5C%5C%20Q%20%3D%20Q_B&plus;Q_I%20%3D%20%28x_s-W_%7BDn%7D%29N_D&plus;C_%7Box%7D%28V_G-V_%7BFB%7D%5E*%29%20%5C%5C%20for%20%5C%3B%5C%3B%5C%3B%20V_%7BFB%7D%5E*%3CV_G)

Given the channel charge, the drain current can be calculated in a way similar to those previously derived. But compared to the surface-channel devices, the buried-channel MOSFET equations are more complicated since the coupling of the gate to the channel (or net gate capacitance) is now gate-bias dependent. Qualitative I- V characteristics are shown in the following figure.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/I_V_Buirried.png)

More-exact solution of the drain current can be obtained by substituting the charge into ID integrangd Eq. The results, divided into different regimes of V, bias, are summarized in Table 1. These results are based on the long-channel constant-mobility model. Current saturation due to velocity saturation can be estimated to be = Qν<sub>s</sub>W.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Table_Buried_Current.png)

A buried-channel MOSFET is usually normally-on (depletion-mode), although theoretically it can be made as a normally-off (enhancement-mode) device, by proper choice of metal work function, for example. Also for a given ND, the threshold voltage becomes more negative with increased buried-channel depth xs. However, because there exists a maximum depletion width in an MOS system, if the doping density ND or/and the buried-channel depth xs are sufficiently large, WDs can reach a maximum value without pinching off the channel. A limit on the channel profile thus exists, otherwise the transistor cannot be turned off. This condition is bound by a combination of xs and ND;

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20x_s%7C_%7Bmax%7D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_D%7D%7D%28%5Csqrt%7B2%5Cpsi_B%7D&plus;%5Csqrt%7B%5Cfrac%7BN_A%5Cpsi_%7Bbi%7D%7D%7BN_A&plus;N_D%7D%7D%29)

In the buried-channel devices, the substrate-bias effect is more direct. It can be viewed as a bottom gate. The effects are calculated in the above equations if ψ<sub>bi</sub> is replaced with ψ<sub>bi</sub> - V<sub>BS</sub> (V<sub>BS</sub> is negative). In particular, V<sub>T</sub> (Eq. 6) and W<sub>Dn</sub> (Eq. 7) can be shifted with a substrate bias, to the extent that the transistor can be turned on and off and between depletion-mode and enhancement-mode.

We now turn to the subthreshold current of buried-channel devices. At a sufficiently large negative gate bias, the channel will be pinched off, that is, when x<sub>x</sub> = W<sub>Ds</sub> + W<sub>Dn</sub> (below Fig. c). The conduction below the threshold voltage is due to the presence of a region of partially depleted electrons, wherein the current is carried primarily by difision of electrons. The resulting subthreshold (sub-pinch-off) current for a
buried-channel MOSFET is, thus, directly analogous to the subthreshold current for a surface-channel MOSFET. The subthreshold current will vary exponentially with the gate voltage, and the subthreshold swing S is given by the capacitive divider ratio again of Eq. 60, except now different capacitances have to be used. From Fig. c the maximum electron concentration occurs at the location of x = xs - WDn. So CD of Eq. 60 should be replaced with the depletion capacitance of the substrate p-n junction [ε<sub>s</sub>/(WDn + WDp)], and C<sub>ox</sub> should be replaced with C<sub>ox</sub> in series with the surface depletion capacitance ε<sub>s</sub>/WDs. These substitutions give an expression of

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Buried_Band_Diag.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20S%20%3D%20ln%2810%29%5Cfrac%7BkT%7D%7Bq%7D%5B1&plus;%5Cfrac%7B%5Cepsilon_%7Box%7DW_%7BDs%7D&plus;%5Cepsilon_sd%7D%7B%5Cepsilon_%7Box%7D%28W_%7BDn%7D&plus;W_%7BDp%7D%29%7D%5D)

where all depletion layers WDs, WDn, and WDp correspond to the condition at threshold (VG = VT). The subthreshold swing is usually larger than that of conventional surface-channel devices.

The buried-channel device is expected to have higher carrier mobility than surface-channel devices since carriers are free of surface scattering and other surface effects. They are also less affected by the short-channel effects (to be discussed next) such as hot-carrier-induced reliability problems. On the other hand, since the net distance between the gate and the channel is further away and is gate-bias dependent, the transconductance is smaller and variable. Note that if the gate is replaced by a Schottky junction or a p-n junction, the device become a MESFET or a JFET correspondingly.

## Device Scaling and Short-Channel Effects
1) As the channel length decreases, the depletion widths of the source and drain become comparable to the channel length and punch-through between the drain and source will eventually occur. This requires higher channel doping. A higher channel doping will increase the threshold voltage, and in order to control a reasonable threshold voltage, a thinner oxide is necessary.

2) Even with the best scaling rules, as the channel length is reduced, departures from long-channel behavior are inevitable. These departures, the short-channel effects, arise as results of a two-dimensional potential distribution and high electric fields in the channel region. The potential distribution in the channel now depends on both the transverse field ξ<sub>x</sub> (controlled by the gate voltage and the back-substrate bias) and the longitudinal field ξ<sub>y</sub> (controlled by the drain bias). In other words, the potential distribution becomes two-dimensional, and the gradual-channel approximation (that is, ξ<sub>x</sub> >> ξ<sub>y</sub>) is no longer valid. This two-dimensional potential results in many forms of undesirable electrical behavior.

3) As the electric field is increased, the channel mobility becomes field-dependent, and eventually velocity saturation occurs. When the field is increased further, carrier multiplication near the drain occurs, leading to substrate current and parasitic bipolar-transistor action. High fields also cause hot-carrier injection into the oxide leading to oxide charging and subsequent threshold-voltage shift and transconductance degradation.

These aforementioned phenomena will cause short-channel effects which can be summarized as follows: (1) V<sub>T</sub> is not constant with L, (2) I<sub>D</sub> does not saturate with V<sub>D</sub> bias, both above and below threshold; (3) I<sub>D</sub> is not proportional to 1/L; and (4) device characteristics degrade with operation time.

### Device Scaling
The most-ideal scaling rule to avoid short-channel effects is simply to scale down all dimensions and voltages of a long-channel MOSFET so that the internal electric fields are kept the same, as shown in the following table and figure. The doping level is increased by K, and all voltages are reduced by K, leading to a reduction of the junction depletion width by about K. Note that the subthreshold swing S remains essentially the same since S is proportional to 1 + Cd/Cox, and both capacitances are scaled up by the same factor K.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Scale_factor.png)

Unfortunately such an ideal scaling rule is hindered by other factors that are fundamentally not scalable. 1) First, the junction built-in voltage and the surface potential for the onset of weak inversion do not scale (only 10% change for 10 times increase in dopings). These limitations stem from the fact that both the energy gap and thermal energy kT remain constant. 2) The gate oxide thickness has the technological difficulty of defects as it approaches the low-nm scale. 3) Tunneling through the oxide is another findamental limitation. 4) The quantum-mechanical effect discussed previously degrades the gate capacitance due to the fact that carriers are located at a finite distance (l nm) from the interface. 5) The source and drain series resistance
increases when rj is decreased. This is especially detrimental when the current of the device increases at the same time. 6) The channel doping cannot be increased indefinitely due to p-n junction breakdown. 7) The threshold voltage cannot be scaled due to the off-current consideration, even with a fixed subthreshold swing. 8) The supply voltage has been historically slow in scaling because of the system consideration, and also the push for higher speed. With these limitations, the field is no longer kept the same, and it increases with smaller gate lengths. 

With the above practical limitations, other scaling rules have been proposed. These include constant-voltage scaling, quasi-constant-voltage scaling and generalized scaling. One other scaling rule with a unique feature of having flexible scaling factors has been proposed. This allows the various device parameters to be adjusted independently as long as the overall behavior is preserved. Therefore, all device parameters do not have to be scaled by the same factor K. The expression for minimum channel length for which long-channel behavior can be observed is found to follow a simple empirical relation:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20L%20%5Cgeqslant%20C_1%5Br_jd%28W_D&plus;W_s%29%5E2%5D%5E%7B1/3%7D%20%5C%5C%5C%5C%20W_D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_A%7D%28V_D&plus;%5Cpsi_%7Bbi%7D-V_%7BBS%7D%29%7D)

where C1 is a constant, and WS + WD is the sum of the source and drain depletion widths in a one-dimensional abrupt junction formulation. For VD = 0, WD equals WS. 

We have discussed the nonideal factors that hinder constant-field scaling, resulting in some form of a penalty. On the positive notes, there are a couple of disruptive technologies on the horizon that will help scaling. First, MOSFETs built on a three-dimensional structure with an ultra-thin body will effectively eliminate most the conduction path for punch-through, and the requirement on channel doping can be relaxed. Second, research activities looking for gate dielectrics with high dielectric constants have been intense. Such a high-K gate dielectric can relax the physical thickness, improving the defect density and reducing the field for tunnelling. Both of these technologies can help to circumvent or delay the short-channel effects for a particular generation of channel length.

### Charge Sharing from Source/Drain
Analysis of the channel charge so far is 1-dimensional, that is, both the inversion charge and depletion charge is completely balanced by the charge on the gate, so they can be treated as charge density. Detailed 2-dimensional examination at the ends of the channel reveals that some of the depletion charge is balanced by the n+-source and drain, as shown in the following Fig a. Departure from long-channel behavior can be shown to happen by applying the charge conservation principle to the region bounded by the gate, the channel, and the source/drain. 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Source_Drain_Sharing.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_M%27&plus;Q_n%27&plus;Q_B%27%20%3D%200%20%5C%5C%5C%5C%20V_T%20%3D%20V_%7BFB%7D&plus;2%5Cpsi_B&plus;%5Cfrac%7BQ_B%27%7D%7BC_%7Box%7DA%7D)

where Q<sub>M</sub>' is the total charge on the gate, Q<sub>n</sub>' is the total inversion-layer charge, Q<sub>B</sub>' is the total ionized impurity in the depletion region, and A is the gate area ZxL. For long-channel devices, Q<sub>B</sub>'=qN<sub>A</sub>AW<sub>Dm</sub>, where W<sub>Dm</sub> is the maximum depletion-layer width. 

For short-channel devices, the full effect of Q<sub>B</sub>' on the threshold voltage is reduced, because near the source and drain ends of the channel, some field lines originating from the bulk charges under the channel region terminate at the source or drain instead of the gate (Fig. 26a). Note that the horizontal depletion-layer widths y<sub>S</sub> and y<sub>D</sub> (above fig a) are smaller than the vertical depletion-layer widths W<sub>S</sub> and W<sub>D</sub>, respectively, because the transverse field strongly influences the potential distribution at the surface.

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_B%27%20%3D%20ZqN_AW_%7BDm%7D%28%5Cfrac%7BL&plus;L%27%7D%7B2%7D%29%20%5C%5C%5C%5C%5C%5C%20L%27%20%3D%20L%20-2%28%5Csqrt%7Br_j%5E2&plus;2W_%7BDm%7Dr_j%7D%20-%20r_j%29%20%5C%5C%5C%5C%5C%5C%20%5CDelta%20V_T%20%3D%20%5Cfrac%7B1%7D%7BC_%7Box%7D%7D%28%5Cfrac%7BQ_B%27%7D%7BZL%7D-qN_AW_%7BDm%7D%29%20%5C%5C%5C%5C%20%3D%20-%5Cfrac%7BqN_AW_%7BDm%7D%7D%7BC_%7Box%7D%7D%281-%5Cfrac%7BL&plus;L%27%7D%7B2L%7D%29%20%5C%5C%5C%5C%20%3D%20-%5Cfrac%7BqN_AW_%7BDm%7Dr_j%7D%7BC_%7Box%7DL%7D%28%5Csqrt%7B1&plus;%5Cfrac%7B2W_%7BDm%7D%7D%7Bj%7D%7D-1%29)

The negative sign means VT is lowered and the transistor is easier to turn on. To take into account the effect of the drain voltage and the substrate bias, Eq. 99 can be modified to read:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5CDelta%20V_T%20%3D%20%3D%20-%5Cfrac%7BqN_AW_%7BDm%7Dr_j%7D%7BC_%7Box%7DL%7D%20%5C%5C%5C%5C%20%5Ctimes%5B%28%5Csqrt%7B1&plus;%5Cfrac%7B2y_s%7D%7Bj%7D%7D-1%29&plus;%28%5Csqrt%7B1&plus;%5Cfrac%7B2y_d%7D%7Bj%7D%7D-1%29%5D%20%5C%5C%5C%5C%5C%5C%20y_s%20%5Capprox%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_A%7D%28%5Cpsi_%7Bbi%7D-%5Cpsi_s-V_%7BBS%7D%29%7D%20%5C%5C%5C%5C%20y_s%20%5Capprox%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_A%7D%28%5Cpsi_%7Bbi%7D&plus;V_D-%5Cpsi_s-V_%7BBS%7D%29%7D)

Note that the threshold voltage becomes a function of both L and VD. 

The above figure a also shows that yD is a high-field region where carriers are swept out efficiently. ys is a transitional region where the electron concentration is higher than that in the main channel. So for consideration of the channel drift region, the effective channel length is more meaningful, given by: 

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20L_%7Beff%7D%20%3D%20L%27%20%3D%20L%20-%20y_s%20-%20y_D)

This factor contributes to a drain-bias dependence of the effective channel length and partially accounts for the nonsaturating current with drain bias. Nevertheless, the change of channel length affects the current only linearly, whereas the barrier lowering caused by the drain bias, considered next, is much more pronounced since the current has an exponential dependence on the barrier.

### Drain-Induced Barrier Lowering (DIBL)
We have pointed out that when the source and drain depletion regions are a substantial fraction of the channel length, short-channel effects start to occur. In extreme cases when the sum of these depletion widths approaches the channel length (ys +yD ≈ L), more-serious effects will happen. This condition is commonly called punch-through. The net result is a large leakage current between the source and drain, and that this current is a strong function of the drain bias.

The origin of punch-through is the lowering of the barrier near the source, commonly referred to as DIBL (drain-induced barrier lowering). When the drain is close to the source, the drain bias can influence the barrier at the source end, such that the channel carrier concentration at that location is no longer fixed. This is demonstrated by the energy bands along the semiconductor surface, shown in the following figure. For a long-channel device, a drain bias can change the effective channel length, but the barrier at the source end remains constant. For a short-channel device, this same barrier is no
longer fixed. The lowering of the source barrier causes an injection of extra carriers, thereby increasing the current substantially. This increase of current shows up in both above-threshold and subthreshold regimes.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/DIBL.png)

An example of severe punch-through characteristics above threshold is shown in the following Fig. a. For this device, at VD = 0 the sum of ys and yD is 0.26 um which is larger than the channel length of 0.23 um. Therefore, the depletion region of the drain junction has reached the depletion region of the source junction. Over the drain bias range shown, the device is operated in punch-through condition. Under such a condition, majority carriers in the source region (electrons in this case) can be injected into the depleted channel region, where they will be swept by the field and collected at the
drain. The punch-through drain voltage and current (dominated by the space-charge-limited current) can be estimated by the depletion approximation to be:

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Punch_Current.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7Bpt%7D%20%5Capprox%20%5Cfrac%7BqN_A%28L-y_s%29%5E2%7D%7B2%5Cepsilon_s%7D-%5Cpsi_%7Bbi%7D%20%5C%5C%5C%5C%5C%5C%20I_D%20%5Capprox%20%5Cfrac%7B9%5Cepsilon_s%5Cmu_nAV_D%5E2%7D%7B8L%5E3%7D)

where A is the cross-sectional area of the punch-through path. The space-charge-limited current increases with V<sub>D</sub><sup>2</sup> and is parallel to the inversion-layer current. The calculated points in the figure are from a 2-dimensional computer calculation incorporating the punch-through effect and field-dependent mobility effect.

The DIBL effect on subthreshold current is shown in Fig. b, for various channel lengths. The device with a 7-um channel length shows long-channel behavior, that is, the subthreshold drain current is independent of drain voltage when VD > 3kT/q. For L = 3 um, there is a substantial dependence of current on VD, with a corresponding shift of VT (which is at the point of current departure of the I-V characteristic from the straight line). The subthreshold swing also increases. For an even shorter channel, L = 1.5 um, long-channel behavior is totally lost. The subthreshold swing becomes much worst and the device cannot be turned off any more.

### Multiplication and Oxide Reliability
We pointed out earlier that due to nonideal scaling, the internal electric fields in MOSFETs would increase with shorter channel lengths. In this section we discuss the anomalous currents associated with high fields, as well as their impacts. The following figure depicts all parasitic currents in addition to the main channel current. Note that the highest field occurs near the drain, and this is the location where most of the anomalous currents originate.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/parasitic_current.png)

First, as the channel carriers (electrons) go through the high-field region, they acquire extra energy from the field without losing it to the lattice. These energetic carriers are called hot carriers whose kinetic energy is measured above the conduction band Ec. This extra energy, if larger than the Si/Sio2 barrier (3.1 eV), enables them to escape to the oxide layer and to the gate terminal, and gives rise to a gate current. Another major phenomenon happening in the high-field region is impact ionization which generates extra electron-hole pairs. These extra electrons go directly to the drain and add to the channel current. The path of the generated holes, however, is more diverse. A small fraction of them are driven to the gate, analogous to the hot
electrons mentioned before. The majority of the generated holes flow to the substrate. For short-channel devices, some holes will go to the source. The division of these paths depends on how good the substrate tie is. A perfect substrate tie (Rsub = 0) will sink all the hot holes and none of them will go to the source. As explained later, holes going to the gate or source will produce undesirable effects.

An example of the MOSFET terminal currents, including the gate current and substrate current, are shown in the following Fig. Note that the gate current is due to hot electrons and hot holes over the barrier and is different from carriers tunneling through the barrier. This hot-carrier gate current peaks approximately at VG = VD. It is generally very small, and it by itself does not post a problem since it is negligible compared to the channel current. The impacts are the damages it creates. It is well known that these hot carriers create oxide charges and interface traps. As a result, device characteristics change with operation time. In particular, the threshold voltage shifts, generally to a higher value, and the transconductance g, degrades because of interface traps and reduced channel mobility. The subthreshold swing becomes larger because of increased interface-trap density. To reduce oxide charging, the density of water-related traps in the oxide should be minimized, because such traps are known to capture hot carriers on their passage. In order to ensure MOSFETs’ performance over a reasonable time, it is important to quantify the device lifetime over which the device parameters do not drift outside a given range, for a given bias condition. This is part of the specification of a MOSFET technology.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/ID-IBS-IG.png)

The figure also shows the general characteristics of the substrate current. The substrate current has a unique bell shape as a function of gate bias. It increases first with VG, reaches a maximum then decreases. This maximum occurs usually around V<sub>G</sub>≈V<sub>D</sub>/2. The maximum in I<sub>BS</sub> can be explained as follows. Assuming that the impact ionization occurs uniformly in the high-field region, the substrate current can be written as 
I<sub>BS</sub> ≈ I<sub>D</sub>α(ξ)y<sub>D</sub>, where α(ξ) is the ionization coefficient, the number of electron-hole pairs generated per unit distance, and is a strong function of the electric field; and y<sub>D</sub> is the high-field or pinch-off region. For a given V<sub>D</sub>, as V<sub>G</sub> increases, both I<sub>D</sub> and V<sub>Dsat</sub> increase (V<sub>Dsat</sub> ≈ V<sub>G</sub> - V<sub>T</sub>). When V<sub>Dsat</sub> increases, the lateral field [= ( V<sub>D</sub>- V<sub>Dsat</sub>/y<sub>D</sub>] decreases, causing a reduction of α. Maximum I<sub>BS</sub> occurs where the two factors balance each other. Empirically, the substrate current can be expressed as (where C2 and C3 are constants):

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BBS%7D%20%3D%20C_2I_D%28V_D-V_%7BDsat%7D%29exp%28%5Cfrac%7B-C_3%7D%7BV_D-V_%7BDsat%7D%7D%29)

For a short-channel device, that is, a small source-drain separation, avalanched holes have increasing tendency to flow to the source. 1) This hole current constitutes a base current of a parasitic n-p-n bipolar-transistor action, where source-substrate-drain is equivalent to the emitter-base-collector configuration. For every hole that goes to the source, there are many electrons injected to the substrate. These electrons will be collected by the drain and show up as additional drain current. This bipolar current gain I<sub>n</sub>/I<sub>p</sub> is roughly determined by the ratio of N<sub>D</sub>/N<sub>A</sub>. 2) Another way to look at this is that the substrate current develops a substrate voltage I<sub>BS</sub>R<sub>sub</sub> which puts the
source-substrate p-n junction under forward bias, thereby injecting electrons into the substrate. 3) An additional effect is that the higher substrate potential lowers the threshold voltage for the surface channel and increases the surface-channel current. Both effects will increase the total drain current. These effects will become worst with an increase of R<sub>sub</sub> and shorter L. In the extreme case of a MOSFET without a substrate contact (R<sub>sub</sub> = ∞) such as an SOI or TFT structure, the output curves show sudden rise of ID with VD. This is referred to as kink effect in the output characteristics.

In more-severe cases, the substrate current can induce source-drain breakdown from this parasitic n-p-n bipolar action. Analogous to the analysis of a bipolar break-down, since the source-drain distance is much shorter than the drain-to substrate contact, the base can be treated as open, and the MOSFET source-drain breakdown is given by the parasitic open-base bipolar breakdown:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BBDS%7D%20%5Capprox%20%5Cfrac%7BV_%7BBDx%7D%7D%7B2%5E%7B1/n%7D%7D%28%5Cfrac%7BL%7D%7BL_n%7D%29%5E%7B2/n%7D)

Here V<sub>BDx</sub> is the drain-substrate p-n junction breakdown voltage, and n describes the shape of this diode breakdown characteristics. the L (channel length) is the effective base width, and L<sub>n</sub> is the electron difision length in the substrate. The difference in breakdown voltage for different junction curvature can be explained by the dependence of V<sub>BDx</sub> on r<sub>j</sub>, as discussed in p-n junction chapter. To reduce the parasitic transistor effect, the resistance of the substrate R<sub>sub</sub> should be minimized so that the product of I<sub>BS</sub>R<sub>sub</sub> remains smaller than = 0.6 V. Then the breakdown voltage of a short-channel MOSFET will no longer be limited by this parasitic bipolar effect, and higher voltages and more-reliable operation can be expected.

The drain-gate overlap region forms a gated-diode structure. For a thin oxide together with an abrupt junction, avalanche can occur during certain bias condition and it results in a drain leakage current going to the substrate. Such gated-diode avalanche current is called gate-induced drain leakage (GIDL) and the mechanism has been discussed in more details in Section 2.4.3. For an n-channel device, with a fixed drain bias, the normal channel current decreases with decreasing gate bias into the subthreshold regime. At some gate bias, the drain current becomes the GIDL current, and it rises again with more negative gate bias. Very often, in short-channel devices, this GIDL current already exists at VG= 0, imposing a leakage current component in
their off-state.

## MOSFET Structers
Many device structures have been proposed to control short-channel effects and improve MOSFET performance. We shall now consider the MOSFET structure
broken down here into separate parts: channel doping, gate stack, and source/drain design. This is followed by some representative device structures for ultimate perfor mance and special purposes.

### Channel Doping Profile
The following figure shows the schematic of a typical high-performance MOSFET structure based on planar technology. The channel doping profile has a peak level slightly below the semiconductor surface. Such a retrograde profile is achieved with ion implantation, often of multiple doses and energies. The low concentration at the surface has the advantages of higher mobility due to reduced normal field and low threshold voltage. The high peak concentration below the surface is to control punch-through and other short-channel effects. Lower concentration is typically below the junction depth. It reduces the junction capacitance as well as the substrate-bias effect on threshold voltage.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/channel_profile.png)

### Gate Stack
The gate stack consists of the gate dielectric and the gate contact material. The gate material has been polysilicon for a long time. The advantages of a
poly-Si gate is (1) its compatibility with the silicon processing, and (2) its ability to withstand high-temperature anneal that is required after self-aligned source/drain implantation. (3) Another important factor is that the work function can be varied by doping it into n-type and p-type. Such flexibility is crucial for a symmetric CMOS technology. (1) One limitation of the poly-Si gate is its relatively high resistance. This does not result in penalty of dc characteristics since the gate terminates on the gate insulator. (2) Another shortcoming of poly-Si gate is the finite depletion width at the oxide interface. This reduces the effective gate capacitance and becomes more severe with thinner oxides. To circumvent the problems of resistance and depletion, gate materials of silicides and metals are obvious choices. Potential candidates are TiN, TaN, W, Mo, and NiSi.

### Source/Drain Design
Details of the source/drain structures are shown in the above figure. Typically the junction has two sections. The extension near the channel has shallower junction depth to minimize short-channel effects. Sometimes it is doped less heavily to reduce the lateral field for consideration of hot-carrier aging. For this purpose it is called a lightly doped drain (LDD). The deeper junction depth away from the channel helps to minimize the series resistance.

It has been pointed out that the sharpness or gradient of the source/drain profile is critical to minimize the series resistance. We refer to the following figure to understand its origin. In practice the profile is never perfectly abrupt, and there exists a region of accumulation layer (of n-type) before current spreads into the bulk of the source/drain. This accumulation-layer resistance R<sub>ac</sub> is related to the transition distance before the doping reaches a critical level.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/parasitic_Resistance.png)

A major milestone for source/drain design is the development of the silicide contact technology which started in the early 1990s. Unlike the metal contact, the silicide can be made self-aligned to the gate, as shown in Fig. 32, thus minimizing the sheet-resistance component (R<sub>sh</sub>) between the contact and the channel. In this way the silicide has become the metal contact because contact resistance between metal and silicide is very small. This self-aligned silicide process has been coined salicide. The salicide process is described as follows. After the gate definition, an insulator spacer
is formed on the sides of the gate. A metal layer for silicidation is deposited uniformly, which at this stage is shorting the gate and the source/drain. After a thermal reaction at low temperature (≈ 450°C), the metal reacts with silicon to form silicide on the sourceldrain region. Silicide formation on the gate is optional depending on whether the gate is capped with an insulation layer as part of the gate stack. Metal over the spacer region and the field region (between transistors, not shown) remains metal since there is no exposed silicon for reaction. The metal is then removed with a selective chemical that etches metal only without etching silicide, thereby removing the shorting paths. Note that the silicide/silicon interface in Fig. 32 is slightly
recessed. This is due to the consumption of silicon during silicide formation. Examples for salicides are CoSi2, NiSi2, TiSi2, and PtSi.

### Schottky-Barrier Source/Drain
Instead of p-n junction, use of Schottky-barrier contacts for the source and drain of a MOSFET can result in some advantages in fabrication and performance. The following figure shows a schematic MOSFET structure with such Schottky source and drain.61 For a Schottky contact, the junction depth can
effectively be made zero to minimize the short-channel effects. n-p-n bipolar-transistor action is also absent for undesirable effects such as bipolar breakdown and latch-up phenomenon in CMOS circuits. Eliminating high-temperature implant anneal can promote better quality in the oxides and better control of geometry. In addition, this structure can be made on semiconductors such as CdS where p-n junctions cannot be easily formed.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Schottky_MOS.png)

The figure above b-d show the working principle of a Schottky source/drain. At thermal equilibrium with VG = VD = 0, the barrier height of the metal to the p-substrate for holes is qφ<sub>B</sub> (e.g., 0.84 eV for an ErSi-Si contact). When the gate voltage is above threshold to invert the surface from p-type to n-type, the barrier height between the source and the inversion layer (electrons) is qφ<sub>B</sub> = 0.28 eV. Note that the source contact is reverse biased under operating conditions (Fig. d). For a 0.28-eV barrier, the thermionic-type reverse-saturation current density is of the order of 1E3 A/cm2 at
room temperature. To increase current density, metals should be chosen to give the highest majority-carrier barrier such that the minority-carrier barrier height is minimized. Additional current due to tunneling through the barrier should help to improve the supply of channel carriers. At the present, making the structure on ap-type Si substrate for n-channel MOSFET is more difficult compared to p-channel device with n-substrate, because metals and silicides that give large barrier heights on p-type silicon are less common.

The disadvantages of the Schottky sourceldrain are high series resistance due to the finite barrier height, and higher drain leakage current. Typical I-V curves show that current is starved at low-drain bias. Also note that as shown in the above Fig., the metal or silicide contact has to extend underneath the gate for continuity. This process is much more demanding than a junction source/drain which is done by self-aligned implantation and diffusion.

### Raised Source/Drain
An advanced design is the raised sourceldrain where a heavily doped epitaxial layer is grown over the sourceldrain regions (The following figure a). The purpose is to minimize junction depth to control short-channel effects. Note that an extension underneath the spacer is still needed for continuity. An alternative is the recessed-channel MOSFET where the junction depth rj is zero or negative (Fig. b). The drawback of the recessed-channel structure, especially for submicron devices, is the difficulty in controlling the contour and the oxide thickness at the corners where the threshold voltage is determined. Also, oxide charging may be worsened because more hot-carrier injection will occur.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/deep_gate.png)

### SOI and Thin-Film Transistor (TFT)
Unlike thin-film transistor, the top silicon layer of an SOI (silicon-on-insulator, the following figure) wafer is high-quality single-crystalline material that is suitable for high-performance and high-density integrated circits. Many forms of SOI structures have been demonstrated with different insulator materials and holding substrates. These include silicon-on-oxide, silicon-on-sapphire (SOS), silicon-on-zirconia (SOZ), and silicon-on-nothing(air gap). In SOS and SOZ technologies, a single-crystalline silicon film is epitaxially grown on a crystalline insulating substrate. The difficulties in these techniques are the material quality when the film gets thinner. Among them SIMOX (separation by implantation of oxygen) where high-dose oxygen is implanted onto a silicon wafer followed by high-temperature anneal to form the buried SiO, layer. Another technique involves bonding of two silicon wafers one of which has an oxidized layer followed by thinning or removal of the majority of the top wafer until a thin silicon layer is left. One technique uses lateral epitaxial growth of silicon over an oxide layer, starting from a seed opening to the substrate. Another uses laser recrystallization, transforming amorphous silicon deposited onto the oxide layer into single-crystalline material, or into poly-crystalline form with large grain size.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/SOI.png)

The advantages of the SOI substrate include improved MOSFET scaling due to its thin body. A thin body can alleviate most problem with punch-through such that the channel can be doped lightly. The subthreshold swing is known to be improved. The buried oxide layer serves as good isolation to reduce capacitance to the substrate, giving rise to higher speed. device isolation is much easier, simply by removing the surrounding thin film. This can significantly improve the circuit density. This type of isolation, as opposed to junction isolation in planar technology, also eliminates latch-up phenomenon in CMOS circuits. The disadvantages of SO1 is higher wafer cost, potentially inferior material properties, the kink effect, and worse heat conduction because of the oxide layer.

Thin-Film Transistor (TFT) ---> The thin-film transistor usually refers to MOSFET as opposed to other kinds of transistors. The structure is similar to MOSFET built on SOI with the exception that the active film is a deposited thin film and that the substrate can be of any form. Because the semiconductor layer is formed by deposition, the amorphous material has more defects and imperfections than in single-crystalline semiconductors, resulting in more complicated transport processes in the TFT. To improve device performance, reproducibility, and reliability, the bulk and interface-trap densities must be reduced to reasonable levels. In a TFT, the current is always very limited due to lower mobility, and leakage current is always higher due to defects. The main applications lie in the areas where a large-area or flexible substrate is required and conventional semiconductor processing is not feasible. A good
example is large-area display where an array of transistors is required to control the array of lighting elements. In such applications, device performance such as current or speed is not critical.

### Three-Dimensional Structures
In device scaling, the optimum design is with MOSFET built on a body of ultra-thin layer such that the body is fully depleted under the whole bias range. A design to achieve this more efficiently is to have a surround gate structure that encloses the body layer from at least two sides. Two examples of these 3-dimensional structures are shown in the following figure. They can be classified according to their current-flow pattern: the horizontal transistor and vertical transistor that both of them are difficult to fabricate. A new set of dificulties arise from the fact that the majority or all of the channel surface is on a vertical wall, for both of these structures. This fact presents great challenges in achieving a smooth channel surface from etching and growth or deposition of gate dielectrics on these surfaces. Formation of the source/drain junction is no longer trivial by means of ion implantation. Salicide formation will also be much more difficult. Whether one of these turns out to be the device choice in the hture remains to be seen.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/3D_device.png)

### Power MOSFETs
In general, power MOSFETs employ thicker oxides, deeper junctions, and have longer channel lengths. These generally post a penalty on device performance such as transconductance (g<sub>m</sub>) and speed (f<sub>T</sub>). Nevertheless, power applications from MOSFETs have been on the rise, for example, due to the increasing demand of cellular phones and cellular base stations which require extra-high voltage. We will present two power structures that are designed for RF power applications.

DMOS ===> As the name implies, in the DMOS (double-diffbsed MOS) transistor shown in the following Fig. a the channel length is determined by the higher diffusion rate of the p-dopant (e.g., boron) compared to the n<sup>+</sup>-dopant (e.g., phosphorus) of the source. This technique can yield very short channels without depending on a lithographic mask. Thep-diffusion serves as channel doping and has good punch-through control. The channel is followed by a lightly doped n<sup>-</sup>-drift region. This drift region is long compared to the channel, and it minimizes the peak electric field in this region by maintaining a uniform field. Usually the drain is located at the substrate contact. The field near the drain is the same as in the drift region, so avalanche breakdown, multiplication, and oxide charging are lessened compared to conventional MOSFETs. However, the threshold voltage V<sub>T</sub> is more difficult to control in a DMOS transistor because the channel doping is no longer constant along its length. Since V<sub>T</sub> is determined by the local doping concentration along the semiconductor surface, varying doping level leads to variations in V<sub>T</sub> as a function of distance and bias. Also
the localization of punch-through control by a thin p-shield region requires a higher doping level compared to a conventional structure and it leads to poorer turn-off behavior for DMOS transistors.

![](vhttps://github.com/rvatanme/Transistors/blob/main/MOSFET/DMOS_LDMOS.png)

LDMOS ===> The major difference of the LDMOS (laterally diffused MOS) transistor (the above Fig. b) from a DMOS transistor is that it has a lateral current-flow pattern. The drift region here is an implanted horizontal region. Such a horizontal arrangement enables the p<sup>+</sup>-substrate to deplete this drift region at high drain bias. Yet at low drain bias its higher doping gives lower series resistance. This drift region, thus, behaves as a nonlinear resistor. At low drain bias, its resistance is determined by 1/nqμ. At high drain bias, this region is fully depleted so a large voltage drop can be supported. This concept is called RESURF (reduced surface field) technology. Becasue of this feature, the drift region can be doped with a higher concentration compared to the DMOS transistor for a lower on-resistance. Another advantage of the LDMOS transistor is that the source can be tied internally to the substrate by a deep p-type diffusion. This avoids using a bond wire that has high inductance to the source. The LDMOS transistor can thus perform at higher speed.

## CIRCUIT APPLICATIONS
### Equivalent Circuit and Microwave Performance
The MOSFET is ideally a transconductance amplifier with an infinite input resistance and a current generator at the output. In practice, however, we have other nonideal circuit elements. An equivalent circuit is shown in the following figure for the common-source connection. 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Equivalent_Circuit.png)

The gate resistance R<sub>G</sub> is associated with the gate contact material over the oxide. The input resistance R<sub>in</sub> is caused by tunneling current through the thin gate insulator, and it also includes any conductance through defects. This of course is a function of the oxide thickness. For a thermally grown silicon dioxide layer, this leakage current between the gate and the channel is negligibly small; thus, the input resistance is very high, one of the main advantages of a MOSFET. For oxides below a thickness of 5 nm, the tunneling current starts to become an important factor. The gate capacitance C<sub>G</sub>' (= C<sub>GS</sub>' + C<sub>DS</sub>') is mostly due to C<sub>ox</sub> multiplied by the active channel area ZxL. In practical devices, the gate extends somewhat above the source and drain regions, and these overlap capacitances add to the total C<sub>G</sub>'. This fringing
effect is also an important contribution to the feedback capacitance C<sub>GD</sub>'. The drain output resistance R<sub>DS</sub> is due to the fact that the drain current does not truly saturate with the drain bias. This effect is especially pronounced for short-channel devices, as part of the short-channel effects discussed earlier. The output capacitance C<sub>DS</sub>' consists mostly of the two p-n junction capacitances connected in series through the semiconductor bulk.

In the saturation region, VD and thus RD has little effect on the drain saturation current. The Rs affects the effective gate bias, and the extrinsic transconductance and the cutoff frequency f<sub>T</sub> is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_%7Bmx%7D%20%3D%20%5Cfrac%7Bg_m%7D%7B1&plus;R_sg_m%7D%20%5C%5C%5C%5C%5C%5C%20f_T%20%3D%20%5Cfrac%7Bg_m%7D%7B2%5Cpi%28C_G%27&plus;C_%7Bpar%7D%27%29%7D%20%3D%20%5Cfrac%7Bg_m%7D%7B2%5Cpi%28C_%7Box%7DZL&plus;C_%7Bpar%7D%27%29%7D)

Another figure-of-merit for microwave performance is the maximum frequency of oscillation f<sub>max</sub>, the frequency at which the unilateral gain becomes unity. It is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20f_%7Bmax%7D%20%3D%20%5Csqrt%7B%5Cfrac%7Bf_T%7D%7B8%5Cpi%20R_GC_%7BGD%7D%27%7D%7D)

So for high-frequency performance, the most-important device parameters are g<sub>m</sub>, R<sub>G</sub>, and all other parasitic capacitances.

### Basic Circuit Blocks
In this section we present the basic digital-circuit building blocks in both logic and memory circuits. The most-basic unit for a logic circuit is the inverter. Different configurations for MOSFET inverters are shown in Fig. 41. 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/CMOS.png)

By far the most common is
the CMOS (complementary MOS) inverter where both n-channel andp-channel transistors are used. This logic consumes very low dc power because when the input is either high or low, one of the transistors in series is off so that there is very little steady-state current (subthreshold current) passing through them. In fact, this is one of the main advantages and applications of MOSFETs where the insulated gate can withstand input voltage of any polarity. Such an arrangement is much more dificult with bipolar transistors or MESFETs without putting a large resistor in front of the input. In an NMOS logic (Fig. 41b), the load of thep-channel transistor is replaced with a depletion-mode n-channel transistor. The advantage is a simpler technology since a p-channel device is not required at the expense of higher dc power. This depletion-mode device with the gate tied to the source is basically a two-terminal nonlinear resistor, which is an improvement compared to a simple resistor load shown in Fig. 41c.

Two basic MOSFET memory cells, for SRAM (static random-access memory) and DRAM (dynamic random-assess memory) circuits, are shown in Fig. 42. The SRAM cell has two CMOS inverters connected back to back. It is a latch and a stable cell but it requires four transistors (six including controls for word line and bit line). The DRAM cell only requires one transistor and, thus, has very high memory density. Its memory information is stored as a charge across the capacitor. Since there is finite leakage of charge in the nonideal capacitor, the cell needs to be refreshed periodically, typically at a frequency of ≈ 100 Hz.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/SRAM_DRAM.png)

## NONVOLATILE MEMORY DEVICES
Semiconductor memory devices are classified as shown in the following Fig. The first division is based on their ability to maintain their states when the power is disconnected. As the names imply, a volatile memory loses the content, but a nonvolatile memory does not need voltage to maintain the data.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Memory_Classification.png)

Before getting into each type of nonvolatile semiconductor memory, we should first clarify the difference between a RAM and a ROM. A RAM (random-access
memory) has an x-y address for each cell, which distinguishes it from other serial memories such as magnetic memory. Strictly speaking, a ROM (read-only memory) also has random-access capability since the addressing architecture is similar. In fact the read processes of the RAM and ROM are almost identical. More appropriately, a RAM is sometimes called a read-write memory. However, the nonvolatile ROM has long started to develop some extent of rewriting capability. So the main difference now between a RAM and a ROM is the ease and frequency of erasing and programming. A RAM has almost equal opportunity of rewrite and read. A ROM in general has much more frequent read than rewrite. It itself has a spectrum of rewriting capability, ranging from a pure ROM without any writing capability to a full-feature EEPROM. Because a ROM is smaller in size and more cost-effective than a RAM, it is used whenever frequent rewriting is not required. With this background, different types of nonvolatile memories are explained below:

1) Mask-programmed ROM: The memory content is fixed by the manufacturer and is not programmable once it is fabricated. Sometimes mask-programmed ROM is
simply referred to as ROM.
2) PROM: Programmable ROM is sometimes called field-programmable ROM or fusible-link ROM. The connectivity of the array is custom programmed using the
technique of fusing or antifusing. After programming, the memory works as a ROM.
3) EPROM: In an electrically programmable ROM, programming is performed by hot-electron injection or tunneling to the floating gate, and it requires biases on both the drain and the control gate. Global erase is by exposure to a UV light or x-ray. Selective erase is not possible.
4) Flash EEPROM: A flash EEPROM, as opposed to a full-feature EEPROM below, can be erased electrically but only by a large block of cells simultaneously. It loses byte selectivity but maintains a one-transistor cell. It is, thus, a compromise between an EPROM and a full-feature EEPROM.
5) EEPROM: In an electrically erasable/programmable ROM, not only can it be erased electrically, but also selectively by byte address. To erase selectively, a select transistor is needed for each cell, leading to a two-transistor cell. This makes it less popular than a flash EEPROM.
6) Nonvolatile RAM: This memory can be viewed as a nonvolatile SRAM, or EEPROM with short programming time as well as high endurance. If technology
allows the aforementioned features, this would be the ideal memory.

When the gate electrode of a conventional MOSFET is modified so that semipermanent charge storage inside the gate stack is possible, the new structure becomes a nonvolatile memory device. The two groups of nonvolatile memory devices are the floating-gate devices and the charge-trapping devices (the following Fig). In both types of devices, charges are injected from the silicon substrate across the first insulator and stored in the floating gate or at the nitride-oxide interface. The stored charge gives rise to a threshold-voltage shift, and the device is at a high-threshold state (programmed). For a well-designed memory device, the charge retention time can be over 100 years. To return to the low-threshold state (erased), a gate voltage or other means (such as ultraviolet light) can be applied to erase the stored charge.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Nonvolatile_Memories.png)

### Floating-Gate Devices
In a floating-gate memory device, charge is injected to the floating gate to change the threshold voltage. The two modes of programming are hot-carrier injection and Fowler-Nordheim tunneling. The following figure shows the mechanisms of hot-carrier injection. Near the drain, the lateral field is at its highest level. The channel carriers (electrons) acquire energy from the field and become hot carriers. When their energy is higher than the barrier of the Si/SiO2 interface, they can be injected to the floating gate. At the same time, the high field also induces impact ionization. These generated secondary hot electrons can also be injected to the floating gate. The hot-carrier injection currents give rise to the equivalence of gate current in a regular MOSFET, and is shown in the following Fig. This gate current peaks at VFG = VD where VFG is the potential of the floating gate.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Floating_Gate.png)

Figure 45b shows the original method of hot-carrier injection using drain-substrate avalanche. In this scheme, the floating-gate potential is more negative such that hot holes are injected instead. This injection scheme is found to be less efficient and is no longer used in practice.

Besides hot-carrier injection, electrons can be injected by tunneling. In this programming mode, the electric field across the bottom oxide layer is most critical. On application of a positive voltage VG to the control gate, an electric field is established in each of the two insulators (Fig. 44b). We have, from Gauss' law and Fowler-Nordheim tunneling transport, that:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cepsilon_1%5Cxi_1%20%3D%20%5Cepsilon_2%5Cxi_2%20&plus;%20Q%20%5C%5C%5C%5C%20V_G%20%3D%20V_1%20&plus;%20V_2%20%3D%20d_1%5Cepsilon_1%20&plus;%20d_2%5Cepsilon_2%20%5C%5C%5C%5C%20%5Cxi_1%20%3D%20%5Cfrac%7BV_G%7D%7Bd_1&plus;d_2%28%5Cepsilon_1/%5Cepsilon_2%29%7D%20&plus;%20%5Cfrac%7BQ%7D%7B%5Cepsilon_1&plus;%5Cepsilon_2%28d_1/d_2%29%7D%20%5C%5C%5C%5C%5C%5C%20J%3DC_4%5Cxi_1%5E2exp%28%5Cfrac%7B-%5Cxi_0%7D%7B%5Cxi_1%7D%29)

where the subscripts 1 and 2 correspond to the bottom and top oxide layer respectively, Q (negative) is the stored charge on the floating gate and C4 and ξ0 are constants in terms of effective mass and barrier height. Using either hot-carrier injection or tunneling as programming mechanism, after charging, the total stored charge Q is equal to the integrated injection current since the gate is floating. This causes a shift of the threshold voltage by the amount:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5CDelta%20V_T%20%3D%20%5Cfrac%7B-d_2Q%7D%7B%5Cepsilon_2%7D)

This threshold-voltage shift can be directly measured as shown in the ID-VG plot (the following fig). Alternately, the threshold-voltage shift can be measured from the drain conductance. The change in V , results in a change in the channel conductance gD of the MOSFET. For small drain voltages, the channel conductance of an n-channel MOSFET is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_D%20%3D%20%5Cfrac%7BI_D%7D%7BV_D%7D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cmu%20C_%7Box%7D%28V_G-V_T%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%3EV_T)

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/I_V_Shift.png)

After altering the charge on the floating gate by Q (negative charge), the go-VG plot shifts to the right by ΔVT. To erase the stored charge, a negative bias is put on the control gate or a positive bias on the sourceldrain. The process is the reverse of the tunneling process described above, and the stored electrons tunnel out of the floating gate to the substrate.

The programming and erasing sequence of a floating-gate memory can be understood with the energy-band diagrams in the following figure. In the following Fig. b, electron injection can be due to hot carriers over the barrier or tunneling through the barrier. Figure c shows that the accumulated negative charge at the floating gate raises the threshold voltage compared to its initial condition in Fig. 47a. The erase is carried out by electron tunneling from the floating gate back to the substrate (Fig. d).

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Tunneling_Injection.png)

In both programming and erasing operations, it is important to modulate the floating-gate potential efficiently by the control-gate applied voltage. An important parameter in the floating-gate memory is the coupling ratio which determines the portion of the control-gate voltage that gets coupled to the floating gate capacitively. This coupling ratio is determined by the capacitance ratio:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20R_%7BCG%7D%20%3D%20%5Cfrac%7BC_2%27%7D%7BC_1%27&plus;C_2%27%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_%7BFG%7D%20%3D%20R_%7BCG%7DV_G)

where VFG is the potential of the floating gate and C1' and C2' are the net capacitances associated with the bottem and top insulator layers, respectively. Note that in practice, the areas of the control gate and the floating gate are not necessarily the same. More often than not, the top control gate wraps
around the floating gate so the top capacitor has a larger area. In practical devices, the bottom layer has a tunnel oxide of = 80 A, while the top insulator stack typically has an equivalent oxide thickness of = 140 A. A larger top area makes up for the difference in capacitance per unit area, and the coupling ratio is typically around 0.5-0.6.

In device structure, the first EPROM was developed using a heavily doped poly-silicon as the floating-gate material (Fig. 44a). The device uses drain-substrate avalanche shown in Fig. 45b and is known as floating-gate avalanche-injection MOS (FAMOS) memory. The polysilicon gate is embedded in oxide and is completely isolated. To inject charge into the floating gate (that is, to program), the drain junction is biased to avalanche breakdown, and holes in the avalanche plasma are injected from the drain region into the floating gate. To erase the FAMOS memory, ultraviolet light or x-ray is used. Electrical erasing cannot be used because the device has no external gate. 

To enable electrical erase, the stacked-gate structure with double-level polysilicon gates has been in popular use (Fig. 44b). The external control gate makes electrical erasing possible and also improves the programming efficiency. An example of the programming transient based on hot-carrier injection is shown in the following Fig.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Program_Time.png)

In EEPROM circuits, it is more common to use tunneling as an injection mechanism for programming. A successful commercial device, called FLOTOX (floating-
gate tunnel oxide) transistor, confines the tunneling process to a small area over the drain, as shown in the following Fig. Typical programming and erasing transients for the FLOTOX transistors are shown in the following Fig.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/FLTOX.png)

After programming, by definition, a long retention time is required for nonvolatile memory operation. The retention time is defined as the time when the stored charge decreases to 50% of its initial value and is expressed by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20t_R%20%3D%20%5Cfrac%7Bln%282%29%7D%7B%5Cnu%20ln%28q%5Cphi_B/kT%29%7D)

where ν is the dielectric relaxation frequency, and φB is the barrier height of the floating gate to oxide. The retention time is very sensitive to temperature. Typical retention times at 125°C and 170°C with φB = 1.7 V are found to be about 100 years and 1 year, respectively.

### Charge-Trapping Devices
MNOS Transistors ===> As a memory device, in the MNOS (metal-nitride-oxide-silicon) transistor, the silicon-nitride layer is used as an efficient material to trap electrons as current passes through the dielectric. Other insulators in place of the silicon-nitride film such as aluminum oxide, tantalum oxide, and titanium oxide have been used but are not as common. Electrons are trapped in the nitride layer close to the oxide-nitride interface. The function of the oxide is to provide a good interface to the semiconductor and to prevent back-tunneling of the injected charge for better charge retention. Its thickness has to be balanced between retention time and programming voltage and time.

The following figure shows the basic band diagrams for the programming and erasing operations. In the programming process, a large positive bias is applied to the gate. Current conduction is known to be due to electrons that are emitted from the substrate to the gate. The conduction mechanisms in the two dielectric layers are very different and have to be considered in series. The current through the oxide J,, is by tunneling. Notice that electrons tunnel through the trapezoidal oxide barrier, followed by a triangular barrier in the nitride. This form of tunneling has been identified as modified Fowler-Nordheim tunneling, as opposed to Fowler-Nordheim tunneling through a single triangular barrier. It has the following form of:

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/MNOS_Band.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20J_%7Box%7D%20%3D%20C_5%5Cxi_%7Box%7D%5E2exp%28-%5Cfrac%7BC_6%7D%7B%5Cxi_%7Box%7D%7D%29)

where ξox is the field in the oxide layer, and C5 and C6 are constants. The current through the nitride layer Jn is controlled by Frenkel-Poole transport, which has the form:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20J_%7Bn%7D%20%3D%20C_7%5Cxi_%7Bn%7Dexp%5B-%5Cfrac%7Bq%28%5Cphi_B-%5Csqrt%7Bq%5Cxi_n/%5Cpi%5Cepsilon_n%7D%29%7D%7BkT%7D%5D)

where ξn and εn are the electric field and permittivity in nitride, φB is the trap level below the conduction band (≈ 1.3 V), and C7 is a constant (3E-9 /Ω.cm). It is known that at the beginning of the programming process, modified Fowler-Nordheim tunneling is capable of a higher current, and current conduction is limited by Frenkel-Poole transport through the nitride layer. When the negative charge starts to build up, the oxide field decreases and the modified Fowler-Nordheim tunneling starts to limit the current. The threshold voltage as a hnction of programming pulse width is shown in the below fig. Initially, the threshold voltage changes linearly with time, followed by a logarithmic dependence, and finally it tends to saturate. This programming speed is largely affected by the choice of oxide thickness; a thinner oxide allows a shorter programming time. Programming speed has to be balanced with charge retention since too thin an oxide will allow the trapped charge to tunnel back to the silicon substrate.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/MNOS_Time.png)

The total gate capacitance CG of the dual dielectrics is equal to the serial combination of their capacitances and the amount of trapped charge density Q near the nitride-oxide interface depends on the trapping efficiency of the nitride and is proportional to the integrated Frenkel-Poole current having passed through it. The final threshold-voltage shift is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20C_G%20%3D%20%5Cfrac%7B1%7D%7B%281/C_%7Box%7D%29&plus;%281/C_n%29%7D%20%3D%20%5Cfrac%7BC_%7Box%7DC_n%7D%7BC_%7Box%7D&plus;C_n%7D%20%5C%5C%5C%5C%5C%5C%20%5CDelta%20V_T%20%3D%20-%5Cfrac%7BQ%7D%7BC_n%7D)

In the erasing process, a large negative bias is applied to the gate. Traditionally, the discharge process is believed due to the tunneling of trapped electrons back to the silicon substrate. New evidence shows that the major process is due to tunneling of holes from the substrate to neutralize the trapped electrons.

The advantages of the MNOS transistor include reasonable speed for programming and erasing, so it is a candidate as a nonvolatile RAM device. It also has superior radiation hardness, due to minimal oxide thickness and the absence of a floating gate. The drawbacks of the MNOS transistor are large programming and erasing voltages and nonuniform threshold voltage from device to device. The passage of tunneling current gradually increases the interface-trap density at the semiconductor surface and also causes a loss of trapping efficiency due to leakage or tunneling of trapped electrons back to the substrate. These result in a narrowing threshold voltage window after many cycles of programming and erasing. The major reliability
problem of the MNOS transistor is the continuous loss of charge through the thin oxide. It should be pointed out that unlike a floating-gate structure, the programming current has to pass through the entire channel region, so that the trapped charge is distributed uniformly throughout the channel. In a floating-gate transistor, the charge injected to the floating gate can redistribute itself within the gate material, and injection can take place locally anywhere along the channel.

SONOS Transistor ===> The SONOS (silicon-oxide-nitride-oxide-silicon) transistor is sometimes called the MONOS (metal-oxide-nitride-oxide-silicon) transistor. It is similar to an h4NOS transistor except that it has an additional blocking oxide layer placed between the gate and the nitride layer, forming an ON0 (oxide-nitride-oxide) stack. This top oxide layer is usually similar in thickness to the bottom oxide layer. The function of the blocking oxide is to prevent electron injection from the metal to the nitride layer during erase operation. As a result, a thinner nitride layer can be used, leading to lower programming voltage as well as better charge retention. The SONOS transistor now replaces the older MNOS configuration, but the operation
principle remains the same.

## Single Electron Transistor
The structure of an SET is represented by the schematic circuit diagram in the following figure. It has a central single-electron island that has to be extremely small. The island is connected between the source and drain via capacitors through which tunneling occurs to conduct current. The third terminal is the insulated gate and its purpose is to control the current between the source and drain, similar to the case of an FET.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/SET.png)

The opportunity to observe quantization of charge comes directly from the small dimension of the single-electron island. The minimum energy needed to transport a single electron charge to and from the island is q<sup>2</sup>/2C<sub>Σ</sub>, where CΣ (= C<sub>S</sub>+C<sub>D</sub>+C<sub>G</sub>) is its total capacitance. This energy also must be much larger than the thermal energy (> 100kT) for experimental observation, requiring that at room temperature, C<sub>Σ</sub> to be on the order of aF (lE-18 F). This necessitates a single-electron island size less than 1-2 nm. It is also interesting to note that this effect does not require the island to be made of semiconductor materials and most reported results are based on metal dots.

The capacitors between the island and the source or drain are characterized by the tunneling resistances R<sub>TS</sub> and R<sub>TD</sub>. These resistances need to be small (thin insulator layers) to conduct a reasonable amount of current. But they are bound in the lower limit by the Uncertainty principle that electrons have to be treated as particles being clearly on either side of the junction. This requires that R<sub>TS</sub> ≈ R<sub>TD</sub> > h/q<sup>2</sup> (≈ 25.8 kΩ).

The basic I-V characteristics of an SET are shown in the following Fig. First, Fig. a shows that at most values of V<sub>G</sub>, there is a knee V<sub>D</sub> below which current is very much suppressed. This threshold drain voltage, caused by Coulomb blockade, is explained later. Another important feature is that this Coulomb blockade can be varied by the gate voltage. At some values of V<sub>G</sub>, the Coulomb blockade totally vanishes. Shown
in Fig. b, the cycle can be repeated many times and is called a Coulomb-blockade oscillation. This is very different from the gate control of a regular transistor, where the current can be turned on or off monotonically.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Coulomb_Blockade.png)

To explain these characteristics, it is best to go back to the simplest structure: a tunneling capacitor as shown in Fig. 53b. Here the capacitor is charged by a small current source, so the junction voltage V<sub>j</sub> will increase until an electron can tunnel. The basis for the Coulomb blockade is that it requires a certain minimum V<sub>j</sub> before there is enough energy for an electron to tunnel. The minimum energy needed is q<sup>2</sup>/2C<sub>j</sub>, which will be the change of energy of the capacitor when an electron tunnels. This is also the same as the energy gained by the electron when tunneling across the capacitor of voltage V<sub>j</sub> giving:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bq%5E2%7D%7B2C_j%7D%20%3D%20qV_j)

So V<sub>j</sub> has to reach q/2C<sub>j</sub> before an electron can tunnel. This threshold voltage is the basis for the Coulomb blockade. Alternatively, one can get the same answer by considering the charging energy (E<sub>ch</sub>) for transferring N<sub>i</sub> number of electrons:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20E_%7Bch%7D%20%3D%20%5Cfrac%7B%28Q_o-N_iq%29%5E2%7D%7B2C_j%7D%20-%20%5Cfrac%7BQ_o%5E2%7D%7B2C_j%7D%20%5C%5C%5C%5C%5C%5C%20%3D%20%5Cfrac%7BN_i%5E2q%5E2%7D%7B2C_j%7D%20-%20N_iqV_j)

where Q<sub>o</sub> is the original charge before tunneling and is equal to V<sub>j</sub>/C<sub>j</sub>. The criterion, for switching to a different state is that E<sub>ch</sub> has to be negative and at minimum. Next, we consider a single-electron box where an island is placed between two capacitors, the same as the situation when the source and drain of an SET is tied together (Fig. 53c). As the gate voltage is increased, the island voltage (V<sub>I</sub>) is also increased accordingly, although scaled down by a factor of C<sub>G</sub>/C<sub>Σ</sub>. Similar to the case above, as soon as the tunneling junction gets above a voltage of q/2C<sub>Σ</sub> one electron starts to tunnel across it. Once an electron has tunneled to the center island, its potential drops by q/C<sub>Σ</sub>. Figure 55 shows the charging of the center island and its potential as a function of the gate voltage. It can be seen that the gate voltage at which multiple values of N<sub>i</sub> can coexist is at:

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/VG_Ni.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_G%20%3D%20%5Cfrac%7Bq%7D%7BC_G%7D%28N_i&plus;%5Cfrac%7B1%7D%7B2%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%289%29)

This condition implies degeneracy: multiple Ni can exist without a change of energy, and one electron can tunnel freely to and from the island. One can imagine that for an SET, if a small bias is applied to the drain, electrons can tunnel from the source to the island freely and subsequently from the island to the drain. This corresponds to the condition of V<sub>G</sub> where the Coulomb blockade disappears in an SET.

Alternatively, one can derive Eq. 9 by considering the charging energy of a single-electron box:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20E_%7Bch%7D%20%3D%20%5Cfrac%7BN_i%5E2q%5E2%7D%7B2C_%5CSigma%7D%20-%20%5Cfrac%7BN_iqV_GC_G%7D%7BC_%5CSigma%7D)

By equating E<sub>ch</sub>(N<sub>i</sub> + 1) = E<sub>ch</sub>(N<sub>i</sub>), the condition of Eq. 9 can be reached. Another approach to understand this is to plot E<sub>ch</sub> vs. charge (N<sub>i</sub>q) for different V<sub>G</sub>, as shown in the following Fig. Remembering that N<sub>i</sub> takes on only integer values, there are only certain values of V<sub>G</sub> where the E<sub>ch</sub> minimum takes on two values of N<sub>i</sub>, a condition of degeneracy. This means that the system can switch between these two states easily without any energy barrier.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Ech_Ni.png)

We can now return to the SET and explain the two most-important phenomena: the Coulomb blockade and its voltage, and the Coulomb-blockade oscillations. For
current to conduct from the source to drain, there are two junctions that electrons have to tunnel through, but there is only one junction that controls the current flow. Using the energy-band diagrams of the following Fig., if the bottleneck is at the junction between the source and the single-electron island, an electron will start to tunnel if that junction voltage exceeds q/2C<sub>Σ</sub>, corresponding to the criterion of and giving a minimum value of V<sub>Σ</sub> (V<sub>Cb</sub>)

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/SET_Band_Diagram.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7BV_DC_D%7D%7BC_%5CSigma%7D&plus;%5Cfrac%7BV_GC_G%7D%7BC_%5CSigma%7D%20%5Cgeqslant%20%5Cfrac%7Bq%7D%7B2C_%5CSigma%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BCb%7D%20%3D%20%5Cfrac%7Bq%7D%7B2C_D%7D-%5Cfrac%7BV_GC_G%7D%7BC_D%7D)

This blockade voltage as a function of V, is shown in the following figure as the line with a negative slope of:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7BdV_%7BCb%7D%7D%7BdV_G%7D%20%3D%20-%5Cfrac%7BC_G%7D%7BC_D%7D)

Conversely, if the tunneling process is initiated by the island-drain junction, electrons start to flow:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_D%20-%20%28%5Cfrac%7BV_DC_D%7D%7BC_%5CSigma%7D&plus;%5Cfrac%7BV_GC_G%7D%7BC_%5CSigma%7D%29%20%5Cgeqslant%20%5Cfrac%7Bq%7D%7B2C_%5CSigma%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BCb%7D%20%3D%20%5Cfrac%7B%28q/2%29%20V_GC_G%7D%7BC_G&plus;C_S%7D%20%5C%5C%5C%5C%5C%5C%20%5Cfrac%7BdV_%7BCb%7D%7D%7BdV_G%7D%20%3D%20%5Cfrac%7BC_G%7D%7BC_G&plus;C_S%7D)

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Coulomb_Blockade_VG.png)

Note that since the current contours follow closely the shape of the Coulomb-blockade diamonds, an SET has both positive and negative transconductance,
depending on the V, range. This is a unique feature that is different from a regular transistor. From the the above equations, an intercept of q/C<sub>Σ</sub> can be obtained which is the maximum Vcb. 

Alternatively, the Coulomb-blockade voltage can be obtained by setting the charging energy negative, either for the island-source junction or the island-drain junction as the current-limiting junction:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20E_%7Bch%7D%28N_i%3D1%29%3D%5Cfrac%7Bq%5E2%7D%7B2c_%5CSigma%7D-q%28%5Cfrac%7BV_DC_D%7D%7BC_%5CSigma%7D&plus;%5Cfrac%7BV_GC_G%7D%7BC_%5CSigma%7D%29%20%5Cleqslant%200%20%5C%5C%5C%5C%5C%5C%20E_%7Bch%7D%28N_i%3D1%29%3D%5Cfrac%7Bq%5E2%7D%7B2c_%5CSigma%7D-q%5BV_D%20-%20%28%5Cfrac%7BV_DC_D%7D%7BC_%5CSigma%7D&plus;%5Cfrac%7BV_GC_G%7D%7BC_%5CSigma%7D%29%5D%20%5C%5C%20%5Cleqslant%200)
