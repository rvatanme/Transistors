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
