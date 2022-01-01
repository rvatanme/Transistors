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

The characteristics of the surface space charge under the nonequilibrium condition are derived under two assumptions; (1) the majority-carrier quasi-Fermi level E<sub>Fp</sub> is the same as that of the substrate and it does not vary with distance from the bulk to the surface (constant with x), and (2) the minority-carrier quasi-Fermi level E<sub>Fn</sub> is lowered by the drain bias by an amount dependent on the y-position. Based on these assumptions, the one-dimensional Poisson equation for the surface space-charge region at the drain end is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bd%5E2%5Cpsi_p%7D%7Bdx%5E2%7D%20%3D%20%5Cfrac%7Bq%7D%7B%5Cepsilon_s%7D%28N_A-p&plus;n%29%20%5C%5C%5C%5C%20p%3DN_Aexp%28-%5Cbeta%20%5Cpsi_p%29%20%5C%5C%5C%5C%20n%3Dn_%7Bp0%7Dexp%28%5Cbeta%20%5Cpsi_p%20-%20%5Cbeta%20V_D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%20%5Cbeta%20%5Cequiv%20q/kT)

Conceptually the charge due to minority carriers within the inversion layer, is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%7C%20%3D%20q%5Cint_%7B0%7D%5E%7Bx_i%7Dn%28x%29dx%20%3D%20q%5Cint_%7B%5Cpsi_s%7D%5E%7B%5Cpsi_B%7D%20%5Cfrac%7Bn%28%5Cpsi_p%29d%5Cpsi_p%7D%7Bd%5Cpsi_p/dx%7D%20%5C%5C%5C%5C%5C%5C%20q%5Cint_%7B%5Cpsi_s%7D%5E%7B%5Cpsi_p%7D%5Cfrac%7Bn_%7Bp0%7Dexp%28%5Cbeta%5Cpsi_p-%5Cbeta%20V_D%29d%5Cpsi_p%7D%7B%28%5Csqrt2kT/qL_D%29F%28%5Cbeta%5Cpsi_p%2CV_D%2Cn_%7Bp0%7D/p_%7Bp0%7D%29%7D%20%5C%5C%5C%5C%5C%5C%20F%28%5Cbeta%5Cpsi_p%2CV_D%2Cn_%7Bp0%7D/p_%7Bp0%7D%29%5Cequiv%20%5C%5C%5C%5C%20%5Csqrt%7Bexp%28-%5Cbeta%5Cpsi_p%29&plus;%5Cbeta%5Cpsi_p-1&plus;%5Cfrac%7Bn_%7Bp0%7D%7D%7Bp_%7Bp0%7D%7Dexp%28-%5Cbeta%20V_D%29%5Bexp%28%5Cbeta%5Cpsi_p%29-%5Cbeta%5Cpsi_pexp%28%5Cbeta%20V_D%29&plus;1%5D%7D)

where x<sub>i</sub> denotes the point at which qψ<sub>p</sub>(x) = E<sub>Fn</sub> - E<sub>i</sub>(x) = qψ<sub>B</sub>. For the practical doping ranges in silicon, the value ofx, is quite small, of the order of 3 to 30 nm. After some mathematical simplification, the inversion charge Q<sub>s</sub> at the drain end as a function of surface potential can be given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%7C%3D%5Csqrt2qN_AL_D%5B%5Csqrt%7B%5Cbeta%5Cpsi_s&plus;%5Cfrac%7Bn_%7Bp0%7D%7D%7Bp_%7Bp0%7D%7Dexp%28%5Cbeta%5Cpsi_s-%5Cbeta%20V_D%29%7D&plus;%5Csqrt%7B%5Cbeta%5Cpsi_s%7D%5D)

This solution is still difficult to use because at strong inversion, Q<sub>s</sub> is very sensitive to the surface potential. Another shortcoming is that
the relationship to the terminal bias, that is V<sub>G</sub>, is still missing. The charge-sheet model discussed in the following section is simpler and much more useful for deriving the I-V characteristics of MOSFETs.

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
condition 1 , the requirements of zero fixed oxide charge and work-function difference are removed, and their effects are included in a flat-band voltage V<sub>FB</sub> required by the gate to produce the flat-band condition. Consequently V<sub>G</sub> is replaced by V<sub>G</sub> - VV<sub>FB</sub> for the inversion charge, giving:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%28y%29%7C%20%3D%20%5BV_G-V_%7BFB%7D-%28%5CDelta%5Cpsi_i%28y%29&plus;2%5Cpsi_B%29%5DC_%7Box%7D%20%5C%5C%5C%5C%20-%5Csqrt%7B2%5Cepsilon_sqN_A%28%5CDelta%5Cpsi_i%28y%29&plus;2%5Cpsi_B%29%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%281%29)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%28y%29%20%3D%20Z%7CQ_n%28y%29%7C%5Cnu%28y%29%20%5C%3B%5C%3B%5C%3B%5C%3B%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7D%7CQ_n%28y%29%7C%5Cnu%28y%29dy)

where ν(y) is the average carrier velocity. The carrier velocity ν(y) is a function of the y-position since the longitudinal field χ<sub>y</sub>(y) is a variable. Because of this, the relationship between ν(y) and χ<sub>y</sub>(y) is important to evaluate the above equation. We first consider the case where χ<sub>y</sub>(y) is low such that the mobility is constant (for shorter channel lengths, higher field causes velocity saturation and ultimately ballistic transport). Under this assumption, the above equation is simplified to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%3D%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%5C%7B%20%28V_G-V_%7BFB%7D-2%5Cpsi_B-%5Cfrac%7BV_D%7D%7B2%7D%29V_D%20%5C%5C%5C%5C%20-%5Cfrac%7B2%7D%7B3%7D%5Cfrac%7B%5Csqrt%7B2%5Cepsilon_sqN_A%7D%7D%7BC_%7Box%7D%7D%5B%28V_D&plus;2%5Cpsi_B%29%5E%7B3/2%7D-%282%5Cpsi_B%29%5E%7B3/2%7D%5D%5C%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%282%29)

The above equation predicts that for a given V, the drain current first increases linearly with drain voltage (the linear region), then gradually levels off (the nonlinear region), and finally approaching a saturated value (the saturation region). A qualitative discussion of the device operation can be helpful, with the aid of the following Fig. 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/MOSFET_Operated.png)

Let us consider that a positive voltage is applied to the gate, large enough to cause an inversion at the semiconductor surface. If a small drain voltage is applied, a current will flow from the source to the drain through the conducting channel. The channel acts as a resistor, and the drain current I<sub>D</sub> is proportional to the drain voltage V<sub>D</sub>. This is the linear region. As the drain voltage increases, the current deviates from the linear relationship since the charge near the drain end is reduced by the channel potential Δψ<sub>i</sub>. It eventually reaches a point at which the inversion charge at the drain end Q<sub>n</sub>(L) is reduced to nearly zero. This location of Q<sub>n</sub> = 0 is called the pinch-off point. In reality Q<sub>n</sub>(L) is not zero for current continuity, but small because of its high field and high carrier velocity. Beyond this drain bias, the drain
current remains essentially the same, because for VD > VDsat, the pinch-off point starts to move toward the source, but the voltage at this pinch-off point remains the same (VDSat). Thus, the number of carriers arriving at the pinch-off point from the source, and hence the current, remains essentially the same, apart from a decrease in L to the value L' (Fig. c). This change of effective channel length will increase the drain current only when the shortened amount is a substantial fraction of the channel length. This will be considered in the section of short-channel effects.

We shall now consider the current equations for the three cases of linear, non-linear, and saturation regions. In the linear region, with a small VD, using power series around VD and taking only the initial terms, the above equation reduces to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%3D%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%28V_G-V_T-%5Cfrac%7BV_D%7D%7B2%7D%29V_D%20%5C%5C%5C%5C%20for%20%5C%3B%5C%3B%5C%3B%5C%3B%20V_D%3C%3CV_G-V_T)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%3D%20V_%7BFB%7D&plus;2%5Cpsi_B&plus;%5Cfrac%7B%5Csqrt%7B2%5Cepsilon_sqN_A%282%5Cpsi_B%29%7D%7D%7BC_%7Box%7D%7D)

where V<sub>T</sub> is the threshold voltage. 

The pinch-off point occurs because the relative voltage between the gate and the semiconductor is reduced. The drain voltage and the drain current at this point are designated as V<sub>Dsat</sub> and I<sub>Dsat</sub> respectively. Beyond the pinch-off point the current remains independent of V<sub>D</sub> and we have the saturation region. The value of V<sub>Dsat</sub> is obtained from Eq. 1 under the condition Q<sub>n</sub>(L) = 0. The solution yields:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BDsat%7D%20%3D%20%5CDelta%5Cpsi_i%28L%29%20%3D%20V_G%20-%20V_%7BFB%7D%20-%202%5Cpsi_B%20&plus;%20%5C%5C%5C%5C%20K%5E2%5B1-%5Csqrt%7B1&plus;%5Cfrac%7B2%28V_G-V_%7BFB%7D%29%7D%7BK%5E2%7D%7D%5D)

By Substituing V<sub>Dsat</sub> in the equation 2, the saturation current I<sub>Dsat</sub> is obtained as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZ%7D%7B2ML%7D%5Cmu_nC_%7Box%7D%28V_G-V_T%29%5E2%20%5C%5C%5C%5C%20M%5Cequiv%201&plus;%5Cfrac%7BK%7D%7B2%5Csqrt%7B%5Cpsi_B%7D%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20K%20%5Cequiv%20%5Cfrac%7B%5Csqrt%7B%5Cepsilon_sqN_A%7D%7D%7BC_%7Box%7D%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BDsat%7D%20%3D%20%5Cfrac%7BV_G-V_T%7D%7BM%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%283%29)

M has a value slightly larger than unity and it approaches unity with thinner oxide and lower doping. Furthermore, a more convenient form for V<sub>Dsat</sub> can be expressed as above. The transconductance in the saturation region is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20%5Cfrac%7BdI_D%7D%7BdV_D%7D%7C_%7BV_D%20%3E%20V_%7BDsat%7D%7D%20%3D%20%5Cfrac%7BZ%7D%7BML%7D%5Cmu_nC_%7Box%7D%28V_G-V_T%29)

It can be seen here that in this saturation region, for constant mobility, the current is a square-law function according to Eq. 3, indicated by the increasing current steps between gate bias.

Finally, the nonlinear region inbetween these two extreme cases can be described well by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cmu_nC_%7Box%7D%28V_G-V_T-%5Cfrac%7BMV_D%7D%7B2%7D%29V_D)

Equation 1 for the inversion charge is an exact expression. An approximation of the following form, taking advantage of the definition of threshold voltage, can be made:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%7CQ_n%28y%29%7C%20%3D%20C_%7Box%7D%28V_G-V_T-M%5CDelta%5Cpsi_i%28y%29%29)

This simplified charge expression is helpful to analyze the conditions under field-dependent mobility and velocity saturation which is discussed next.

As technology advances and pushes for device performance and density, the channel length gets shorter and shorter. The internal longitudinal field gy in the channel also increases as a result. For low fields, the mobility is constant. This low-field mobility is used for the long-channel characteristics in the last section. In the extreme case of very high field, the velocity approaches a value, saturation velocity ν<sub>s</sub>. In between the constant-mobility regime and the saturation-velocity regime, the carrier velocity can be described by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cnu%28%5Cxi%29%20%3D%20%5Cfrac%7B%5Cmu%5Cxi%7D%7B%5B1&plus;%28%5Cmu%5Cxi/%5Cnu_s%29%5En%5D%5E%7B1/n%7D%7D%20%3D%20%5Cfrac%7B%5Cmu%5Cxi%7D%7B%5B1&plus;%28%5Cxi/%5Cxi_c%29%5En%5D%5E%7B1/n%7D%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%20%284%29)

where μ is the low-field mobility. The value of n changes the shape of the curve, but μ, ν<sub>s</sub>, and the critical field ξ<sub>c</sub> (= ν<sub>s</sub>/μ) remain the same. It has been observed that in silicon for electrons n = 2 and for holes n = 1 have the best fit. The value of ν<sub>s</sub> for electron in silicon at room temperature is around 1E7 cm/s. As the terminal voltage VD is increased from zero, current is increased because of higher field and higher velocity. Eventually the velocity reaches the maximum value of ν<sub>s</sub>, and the current also saturates to a constant value. Notice that this current saturation comes from a completely different mechanism than in the case of constant mobility. Here, it is due to velocity saturation of carriers, before the pinch-off condition can occur.

To derive the I-V characteristics it is important to know the ν-ξ relationship (the following figure). We find that mathematically, for Eq. 4 with n=2, the analysis is rather complicated. Fortunately for the cases of two-piece linear approximation (following figure) and the above equation with n=1, the mathematics is manageable and simple solutions can be obtained. Since these two extremes mostly cover the realistic bounds for different kinds of carriers, we will consider both assumptions.

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/nu_xi_rela.png)

Field-Dependent Mobility: Two-Piece Linear Approximation: In the two-piece linear approximation, the constant-mobility model is valid up to the point when the maximum field near the drain exceeds ξ<sub>c</sub>. Conversely, Eq. 2 is valid up to a new V<sub>Dsat</sub> value which occurs earlier than the constant-mobility model, so the only task is to find the new V<sub>Dsat</sub> which is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BDsat%7D%20%3D%20L%5Cxi_c%20&plus;%20%5Cfrac%7BV_G-V_T%7D%7BM%7D%20-%20%5Csqrt%7B%28L%5Cxi_c%29%5E2%20&plus;%20%28%5Cfrac%7BV_G-V_T%7D%7BM%7D%29%5E2%7D%20%5C%5C%5C%5C%5C%5C%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZC_%7Box%7D%5Cmu_n%7D%7BL%7D%28V_G-V_T-%5Cfrac%7BMV_%7BDsat%7D%7D%7B2%7D%29V_%7BDsat%7D)

Since VDsat here is always smaller than (VG - VT)/M, the field-dependent mobility always gives a lower I<sub>Dsat</sub>.

Field-Dependent Mobility: Empirical Formula. Next we consider the ν-ξ relationship of Eq. 4 with n = 1. Substituting this into I<sub>D</sub> integral equation gives:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BD%7D%20%3D%20%5Cfrac%7BZC_%7Box%7D%5Cmu_n%5Cxi_c%7D%7BL%5Cxi_c&plus;V_D%7D%28V_G-V_T-%5Cfrac%7BMV_%7BD%7D%7D%7B2%7D%29V_%7BD%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BDsat%7D%20%3D%20L%5Cxi_c%5B%5Csqrt%7B1&plus;%5Cfrac%7B2%28V_G-V_T%29%7D%7BML%5Cxi_c%7D%7D-1%5D)

V<sub>Dsat</sub>, has been obtained by setting dI/dV = 0. Again, once V<sub>Dsat</sub> is known, I<sub>Dsat</sub>, can be calculated from the above equation. 

Velocity Saturation. Using either assumption described above, it is interesting and insightful to look at the extreme case of short-channel devices where velocity saturation completely limits the current flow. In such case we set ν = ν<sub>s</sub>, and consequently Q<sub>n</sub> has to be fixed for current continuity, and is approximated to be (VG - VT)Cox. Then ID integrand equation becomes:

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


