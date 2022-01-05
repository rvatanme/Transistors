# Introduction
While in a MOSFET the capacitor is formed by an oxide layer, the JFET (junction FET) and the MESFET (metal-semiconductor FET) form the capacitor by virtue of a depletion layer in a junction; the JFET from ap-n junction and the MESFET from a Schottky (metal-semiconductor) junction. In the branch of HFET (heterojunction FET), a layer of high-bandgap material is grown epitaxially over the channel, and it is used as an insulator. Bear in mind that the conductivity of a material is fundamentally related to its energy gap. An insulator is characterized by having a large energy gap. Epitaxial heterojunction produces an ideal interface. Such technique is necessary when an ideal oxide-semiconductor interface is lacking, which is practically for all semiconductors other than silicon. Under HFETs, the high-bandgap material can be doped or undoped. With high-E, material that is doped, carriers from dopants are transferred to the heterointerface and form a channel of high mobility, since the channel itself is undoped to avoid impurity scattering. This technique is called modulation doping. When applied to the gate of an FET, the result is a MODFET (modulation-doped FET) which possesses some interesting features. When the high-E, material is undoped, the resultant device is called HIGFET (heterojunction insulated-gate FET). In this case modulation doping is not present and the high-E, material is used purely as an insulator. Such a device behaves in principle the same way as a MOSFET.

## JFET AND MESFET
Both JFET and MESFET have the advantage of avoiding problems related to the oxide-semiconductor interface in a MOSFET, such as interface traps and reliability issues arising from hot-electron injection and trapping. However, they have limitation on bias range allowed on the input gate. In comparison, the MESFET offers certain processing and performance advantages over the JFET. The metal gate requires only low-temperature processing compared to ap-n junction made by diffusion or implant-anneal sequence. The low gate resistance and low IR drop along the channel width is a big factor in microwave performance such as noise and f<sub>max</sub>. The metal gate has better control in defining short channel lengths for high-speed applications. It can
also serve as an efficient heat sink for power applications. On the other hand, the JFET has a more robust junction for higher breakdown and power capability. A p-n junction has a higher built-in potential which is useful towards achieving an enhancement-mode device. The higher potential also reduces the gate leakage for the same bias. The p-n junction is a more controlled structure whereas a good Schottky barrier sometimes is difficult to form on certain semiconductors such as some p-type materials. A JFET has more freedom for various gate configurations, such as a heterojunction or a buffered-layer gate, that improve certain aspects of performance. 

### I-V Characteristics
As shown in the following figure, both JFET and MESFET consist of a conductive channel provided with two ohmic contacts, one acting as the source and
the other as the drain. When a positive voltage V<sub>D</sub> is applied to the drain with respect to the source, electrons flow from source to drain. Hence the source acts as the origin of the carriers and the drain as the sink. The third electrode, the gate, forms a rectifying junction and controls the net opening of the channel by varying the depletion width. The rectifying gate is ap-n junction in the JFET and is a Schottky-barrier junction in a MESFET. The device is basically a voltage-controlled resistor, and its resistance can be controlled by varying the width of the depletion layer extending into the
channel region. Most JFETs and MESFETs are of depletion mode, i.e., normally-on with VG = 0, or threshold voltage VG is negative. Very often for JFETs, the channel is surrounded by two gates. For the Fig. below a, that would be a second gate from the bottom side. This type of structure can be bisected into two halves and the final result becomes half of the total values, in both current and transconductance.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/JFET_MESFET.png)

We can divide the characteristic into three regions: the linear region where the drain voltage is small and ID is proportional to VD; the nonlinear region; and the saturation region where the current remains essentially constant and is independent of VD. As the gate bias becomes more negative, both the saturation current IDsat and the corresponding saturation voltage VDsat decrease. 

For deriving general I-V characteristic of JFET or MESFET, we assume that: 1) Channel doping is uniform; 2) The gradual-channel approximation is valid (ξ<sub>x</sub> << ξ<sub>y</sub>); 3) The depletion laye is abrupt; 4) The current gate is niglegeble. We start with the channel charge distribution which is related to the channel dimensions. The channel dimensions and its potential distributions under both gate and drain biases are shown in more details in the following Fig. 

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/JFET_Band_Diagram.png)

Channel-Charge Distribution ===> For a uniformly doped n-channel, under the gradual-channel approximation, the depletion-layer width W, varies only gradually along the channel (x-direction), and one can solve the one-dimensional Poisson equation in the y-direction:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bd%5Cxi_y%7D%7Bdy%7D%20%3D%20-%5Cfrac%7Bd%5E2%5CDelta%20%5Cpsi_i%7D%7Bdy%5E2%7D%20%3D%20%5Cfrac%7BqN_D%7D%7B%5Cepsilon_s%7D%20%5C%5C%5C%5C%5C%5C%20W_D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D%20&plus;%20%5CDelta%20%5Cpsi_i%28x%29%20-%20V_G%29%7D%7BqN_D%7D%7D%20%5C%5C%5C%5C%5C%5C%20%5Cpsi_%7Bbi%7D%20%5Capprox%20%5Cfrac%7B1%7D%7Bq%7D%5BE_g%20-%20kTln%28%5Cfrac%7BN_C%7D%7BN_D%7D%29%5D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20for%5C%3BJFET%20%5C%5C%5C%5C%5C%5C%20%5Cpsi_%7Bbi%7D%20%3D%20%5Cphi_%7BBn%7D%20-%20%5Cfrac%7BkT%7D%7Bq%7Dln%28%5Cfrac%7BN_C%7D%7BN_D%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20for%5C%3BMESFET)

The potential difference Δψ<sub>i</sub>(x) is the potential of the neutral channel [- E<sub>i</sub>(x)/q] with respect to the source. So at the drain end, Δψ<sub>i</sub>(L) = V<sub>D</sub>. The depletion widths at the source and drain ends are given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20W_%7BDs%7D%20%3D%20W_D%280%29%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D%20-%20V_G%29%7D%7BqN_D%7D%7D%20%5C%5C%5C%5C%5C%5C%20W_%7BDd%7D%20%3D%20W_D%28L%29%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D%20&plus;V_D%20-%20V_G%29%7D%7BqN_D%7D%7D)

The maximum value of gate bias applied to increase the current is limited to V<sub>G</sub> = ψ<sub>bi</sub> which corresponds to the condition of W<sub>Ds</sub> = 0. This flat-band condition in practice is not achievable due to the excessive forward current of the gate junction. The maximum value of W<sub>Dd</sub> is equal to a, and the corresponding total band bending is called the pinch-offpotential, defined as: 

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_P%20%5Cequiv%20%5Cfrac%7BqN_Da%5E2%7D%7B2%5Cepsilon_s%7D)

The channel charge density, which is responsible for the current conduction, is proportional to the net channel opening, given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_n%28x%29%20%3D%20qN_D%28a-W_D%28x%29%29%20%5C%5C%5C%5C%20I_D%28x%29%20%3D%20ZQ_n%28x%29%5Cnu%28x%29%20%5C%5C%5C%5C%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7DQ_n%28x%29%5Cnu%28x%29dx%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%281%29)

Equation 1 requires knowledge of the carrier velocity under an applied field, so the ν-ξ relationship is critical. we find that current saturation can
originate from two very different mechanisms. The first is due to channel pinch-off when the net channel is totally pinched off by the depletion width. This is called long-channel behavior, and found to be modelled well simply by a constant mobility. The second possible mechanism, especially true for short-channel devices, is that the field is high enough such that mobility is no longer constant and eventual the velocity rises to a constant value called saturation velocity. This occurs before the channel is pinched off.

Constant Mobility ===> With constant mobility and ξ(x)=dΔψ<sub>i</sub>(x)/dx the following equation is obtained for I<sub>D</sub> in different regiems:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20G_i%5C%7B%7BV_D%20-%20%5Cfrac%7B2%7D%7B3%20%5Csqrt%7B%5Cpsi_P%7D%7D%5B%28%5Cpsi_%7Bbi%7D&plus;V_D-V_G%29%5E%7B3/2%7D-%28%5Cpsi_%7Bbi%7D-V_G%29%5E%7B3/2%7D%5D%7D%5C%7D%20%5C%5C%5C%5C%5C%5C%20G_i%20%3D%20%5Cfrac%7BZq%5Cmu%20N_Da%7D%7BL%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%282%29)

where G<sub>i</sub> is the full channel conductance when W<sub>D</sub> = 0. In the linear region, VD << VG and VD << ψ<sub>bi</sub>, above equation is reduced to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDlin%7D%20%3D%20G_i%281-%5Csqrt%7B%5Cfrac%7B%5Cpsi_%7Bbi%7D-V_G%7D%7B%5Cpsi_P%7D%7D%29V_D%20%5C%5C%5C%5C%5C%5C%20I_%7BDlin%7D%20%3D%20%5Cfrac%7BG_i%7D%7B2%5Cpsi_P%7D%28V_G-V_T%29V_D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%20%5Capprox%20V_T%20%5C%5C%5C%5C%5C%5C%20V_T%20%3D%20%5Cpsi_%7Bbi%7D%20-%20%5Cpsi_P)

When the drain bias continues to increase, the current according to Eq. 2 goes through the nonlinear region. It reaches a peak and actually drops beyond that point. The drop of current is not physical, but it corresponds to a pinch-off condition when W<sub>Dd</sub> = a. The V<sub>D</sub> at the onset of this condition can be shown to occur at:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BDsat%7D%20%3D%20%5Cpsi_P%20-%20%5Cpsi_%7Bbi%7D%20&plus;%20V_G%20%3D%20V_G%20-%20V_T%20%5C%5C%5C%5C%20I_%7BDsat%7D%20%3D%20G_i%5B%5Cfrac%7B%5Cpsi_P%7D%7B3%7D%20-%20%28%5Cpsi_%7Bbi%7D-V_G%29%281-%5Cfrac%7B2%7D%7B3%7D%5Csqrt%7B%5Cfrac%7B%5Cpsi_%7Bbi%7D-V_G%7D%7B%5Cpsi_P%7D%7D%29%5D%20%5C%5C%5C%5C%5C%5C%20g_m%20%5Cequiv%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20G_i%281-%5Csqrt%7B%5Cfrac%7B%5Cpsi_%7Bbi%7D-V_G%7D%7B%5Cpsi_P%7D%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%283%29)

Qualitatively, for drain bias higher than VDsat, the pinch-off point starts to migrate toward the source. However, the potential at the pinch-off point remains to be VDsat, independent of VD. The field within the drift region thus remains fairly constant, giving rise to current saturation. Practical devices show that IDsat does not saturate completely with VD. This is due to the reduction in the effective channel length, which is measured between the source and the pinch-off point. Equation 17 can also be simplified using Taylor's expansion around VG = VT:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%5Capprox%20%5Cfrac%7BG_i%7D%7B4%5Cpsi_P%7D%28V_G-V_T%29%5E2%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%20%5Capprox%20V_T%20%5C%5C%5C%5C%5C%5C%20g_m%20%3D%20%5Cfrac%7BG_i%7D%7B2%5Cpsi_P%7D%28V_G-V_T%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%20%5Capprox%20V_T)

It is seen here that the forms of above equations are similar to that of MOSFET only near the threshold, i.e., VG = VT. This stems from the fact that the gate capacitance (or depletion width) is gate-bias dependent in JFET and MESFET, while that in the MOSFET (gate dielectric) is fixed. In other words, in a MOSFET the channel charge is linearly dependent on VG, while that is not true for a JFET or MESFET. 

Velocity-Field Relationship ===> For long-channel devices, the field is low enough that the carrier velocity is treated as being proportional to the field, i.e., constant mobility. For FETs with short channels, significant discrepancies are encountered between experiment and basic theory. One main reason for the discrepancies is the higher internal field for short channels. The following figure shows the qualitative dependence of the drift velocity versus electric field for silicon. At low fields the drift velocity increases linearly with the field, and the slope corresponds to a constant mobility. At higher fields, the carrier velocity deviates from a linear dependence. It becomes lower than simple extrapolation from the low-field slope, and eventually saturates to a value called saturation velocity νs. So for short-channel devices, these effects have to be taken into account. For silicon the drift velocity approaches its saturation value of lE7 cm/s at fields above 5E4 V/cm. For some semiconductors such as GaAs and InP, the drift velocity first reaches a peak value and then decreases toward a saturation velocity.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Drift_Velocity_E.png)

In this section, we will examine two simple u-E relationships. The first is the two-piece linear approximation shown in the above figure. The second is an empirical formula which has a smooth transition between the constant-mobility regime to the saturation-velocity regime, given as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cnu%28%5Cxi_x%29%20%3D%20%5Cfrac%7B%5Cmu%5Cxi_x%7D%7B1&plus;%28%5Cmu%5Cxi_x/%5Cnu_s%29%7D%20%3D%20%5Cfrac%7B%5Cmu%5Cxi_x%7D%7B1&plus;%28%5Cxi_x/%5Cxi_c%29%7D)

As seen, both relationships contain an important parameter, the critical field ξ<sub>c</sub>

Field-Dependent Mobility: Two-Piece Linear Approximation ===> We first discuss velocity saturation based on the two-piece linear approximation. Note that in this model, the constant-mobility results (i.e., Eq. 2) are valid up to the point where the maximum field, which is at the drain end, reaches the critical field. Once at that VDsat, which is lower than the VDsat of the constant-mobility model, the current saturates at a new and lowered IDsat. So the main task is to calculate this new VDsat. We start with Eq. 1 (and substitute ν = μξ ) which contains the relationship between field and current. Setting ξ=ξ<sub>c</sub> and ID=IDsat, we have:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20Zq%5Cmu%20N_D%20%5Cxi%20_c%5Ba-%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D&plus;V_%7BDsat%7D-V_G%29%7D%7BqN_D%7D%7D%5D%20%5C%5C%5C%5C%5C%5C%20%5Cxi_cL%20%3D%20%5Cfrac%7BV_%7BDsat%7D%20-%20%5B2/%283%5Csqrt%7B%5Cpsi_P%7D%29%5D%5B%28%5Cpsi_%7Bbi%7D&plus;V_%7BDsat%7D-V_G%29%5E%7B3/2%7D-%28%5Cpsi_%7Bbi%7D-V_G%29%5E%7B3/2%7D%5D%7D%7B1-%5Csqrt%7B%28%5Cpsi_%7Bbi%7D&plus;V_%7BDsat%7D-V_G%29/%5Cpsi_P%7D%7D)

Visual examination of this equation indicates that current saturates as VD approaches ξ<sub>c</sub>L , or VD/L ≈ ξ<sub>c</sub>. Once VDsat is known, IDsat can be calculated from Eq. 2 of the constant-mobility model. One also finds that since VDsat is lower than the value from the constant-mobility model, current saturation occurs before the channel is pinched off.

Field-Dependent Mobility: Empirical Formula ===> We next derive the current equation based on the empirical formula given in the above. Substituting this into Eq. 1 and integrating from x = 0 to L , we obtain:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20%5Cfrac%7BG_i%7D%7B1&plus;%28V_D/%5Cxi_cL%29%7D%5C%7B%7BV_D%20-%20%5Cfrac%7B2%7D%7B3%20%5Csqrt%7B%5Cpsi_P%7D%7D%5B%28%5Cpsi_%7Bbi%7D&plus;V_D-V_G%29%5E%7B3/2%7D-%28%5Cpsi_%7Bbi%7D-V_G%29%5E%7B3/2%7D%5D%7D%5C%7D)

Comparing this to Eq. 2, this new result gives a current that is reduced by a factor of (1 + VD/ξ<sub>c</sub>L) from that of the constant-mobility model. In order to obtain VDsat, we seek the current peak from the above equation by setting dID/dVD = 0. This yields a transcendental equation for VDsat. Solutions of VDsat have been calculated and plotted in the following Fig., for various values of ξ<sub>c</sub>L. The top curve (ξ<sub>c</sub>L = ∞) becomes the limit of the constant-mobility model. Note that with decreasing ξ<sub>c</sub>L the saturation of drain current is reached at smaller values of drain voltage.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/VDsat_Psi.png)

Having gone through the three models of u - 8 relationships, it is informative to compare their results on the I-V characteristics. Here we use an example of one I-V curve for a fixed VG (=0) , and the other parameters are; ψP = 4V, ψbi = 1V, and ξ<sub>c</sub>L = 2V. The results are shown in the following fig. The values of the VDsat for the constant mobility, two-piece liner approximation, and the empirical formula are 3V, 1.3V, and 1.9 V respectively. Note that the curve for the two-piece-linear model lies on the constant-mobility curve until VDsat. The lowest current of the three curves corresponds to the empirical formula of Eq. 29 since at any field, the velocity is the lowest among the three models as shown in Fig. 4.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Constant_Peice_Emprical.png)

Velocity Saturation ===> One limiting case is the saturation-velocity model which is expected to be valid in the limit of very short gates where L << VD/ξ<sub>c</sub>. In this assumption, the carriers travel with us in the whole region under the gate, and are totally independent of the low-field mobility. Starting from Eq. 1, the saturation current is simply given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20ZQ_n%5Cnu_s%20%3D%20Zq%28a-W_%7BDs%7D%29N_D%5Cnu_s)

which is reduced from that of the constant-mobility model given by G<sub>i</sub>ψ<sub>P</sub>/3. The choice of depletion width at the source WDs, rather than at the drain is apparent as we discuss details of the carrier-density and velocity profiles in the next section (Dipole-Layer Formation). This equation shows an interesting feature that the saturation current is now totally independent of the channel length. The transconductance is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20-ZqN_D%5Cnu_s%5Cfrac%7BdW_%7BDs%7D%7D%7BdV_G%7D%20%3D%20%5Cfrac%7BZ%5Cepsilon_s%5Cnu_s%7D%7BW_%7BDs%7D%7D)

Since ε<sub>s</sub>/WDS is the gate-source capacitance C<sub>GS</sub> this equation reduces to the familiar FET equation:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20ZC_%7BGS%7D%5Cnu%20_s)

This equation also has the interesting feature that gm is constant and totally independent of gate bias as well as channel length. Olutput characteristics of constant mobility and velocity saturation are compared in the following Fig. Note that the saturation current and saturation voltage are lower under velocity saturation, but the linear regions remain similar. The constant gm under velocity saturation is indicated by the equal spacing of the I-V curves under different VG. As shown, this velocity-saturation limit provides very simple derivations and results, thus giving a good insight of the short-channel
limit. In fact, the simple formulae can fit quite well to the state-of-the-art short channel devices.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Constant_Saturation.png)

Even though velocity saturation sets a limit on the maximum carrier speed in a field-effect transistor, there are two special effects that enable higher speed at part of the channel where the local field is high. The first is related to the material properties, such as in GaAs and InP, which display a transferred-electron effect. At moderately high fields, the drift velocity is actually higher than the saturation velocity. To include this negative-
resistance effect in modeling the I- V characteristics analytically would be very difficult. The second effect is present in ultra-short devices when their channel lengths are comparable to or smaller than the mean free path of scattering. For very short gates, the electrons may not have enough time or distance to reach equilibrium transport in the high-field region of the channel. In such cases, the electrons enter the high-field region and are accelerated to a higher velocity before relaxing to the equilibrium value. Carriers can thus overshoot to more than twice the steady-state velocity and then relax to the equilibrium condition after traveling a certain distance. The overshoot will shorten the electron transit time. This overshoot is expected to improve high-frequency response, especially for the GaAs FET. This phenomenon is related indirectly to low-field mobility since they are both determined by scattering. A material with higher mobility can have more ballistic effect for the same channel length.

Dipole-Layer Formation ===> Below the saturation drain bias VDsat, the potential along the channel increases from zero at the source to VD at the drain. Thus, the gate contact becomes increasingly reverse-biased with respect to the channel, and the depletion width becomes wider as we proceed from source to drain. The resulting decrease in channel opening b must be compensated by an increase in electric field and electron velocity to maintain a constant current throughout the channel. As VD is increased further to VDsat, the electrons reach the saturation velocity at the drain end of the gate (following fig a). The channel is constricted to the smallest cross section b1 under the gate. The electric field reaches the critical value ξ<sub>c</sub> at this point, and , ID starts to saturate. The electron density n(x), however, remains equal to the doping density ND as long as the field does not exceed the critical value ξ<sub>c</sub>. The condition of VD > VDsat is displayed in the following Fig. b. The saturation current is given by:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Dipole_Layer.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20Zq%5Cnu_sn%28x%29b%28x%29)

If the drain voltage is increased beyond VDsat, the depletion region widens toward the drain. The point x1, where the electrons reach the saturation velocity and the channel width is b1, moves toward the source. Note that there are three locations of interest; x1 and x2 are locations where the channel opening is b1, and x1 and x3 are locations where ξ=ξ<sub>c</sub>. This also means that in the region x1 to x2 the channel is narrower than b1, and in the region x1 to x3, carriers travel with ν<sub>s</sub>. Since the velocity is saturated, in the region x1 to x2 the change in channel width must be compensated by a change in carrier density to maintain constant current. According to the above Eq., an electron accumulation layer (n > ND) must form in this region, where the channel opening is smaller than b1. At x2 the channel opening is again b1, and the negative space charge changes to a positive space charge (n < ND) to preserve constant current. Between x1 and x3 the electron velocity remains saturated but the channel width is larger than b1. So by virtue of the same above Eq., carrier concentration is lower than ND in order to keep the saturation current constant. Therefore, the drain voltage applied in excess of VDsat forms a dipole layer in a channel that extends beyond the drain end of the gate.

Breakdown ===> For drain voltages beyond VDsat, the drain current is assumed to remain essentially the same as the saturation current. As the drain voltage increases further, breakdown occurs where the current rises sharply with the drain bias. This breakdown occurs at the gate edge toward the drain side where the field is the highest. The fundamental mechanism responsible for breakdown is impact ionization. Since impact ionization is a strong function of the electric field, the maximum field is often regarded as the first-order criterion for breakdown. Using a simple one-dimensional analysis in the x-direction, and treating the gate-drain structure as a reverse-biased diode, the drain breakdown voltage VDB is similar to that of the gate-junction breakdown and is linearly dependent on the relative voltage of the drain to the gate V<sub>BD</sub> = V<sub>B</sub> - V<sub>G</sub>, where V<sub>B</sub> the breakdown voltage of the gate diode and is a function of channel doping level, among other factors. The general breakdown behavior of the mentioned equation is shown in the following Fig. It is shown that for higher VG, the drain breakdown voltage becomes higher by the same amount. Such characteristics general hold true for silicon JFETs. But for MESFETs on GaAs, the breakdown mechanisms are much more complicated. They generally have lower breakdown values and the dependence of VG no longer follows. 

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/VBD_VG.png)

Unlike a MOSFET where the heavily doped source and drain overlap the gate at the gate edges, the JFETs and MESFETs have a gap between the gate and the
source/drain contacts (or heavily doped regions under the contacts). For breakdown consideration, this gate-drain distance L<sub>GD</sub> is critical. In this gap the doping level is the same as the channel. If surface traps are present in this gate-drain spacing, they can deplete part of the channel doping and affect the field distribution. In certain cases they can improve the breakdown voltage. Two-dimensional simulations in the following fig displays the field distribution as a function of surface potential created by surface traps. Without surface traps (ψ<sub>s</sub> = 0), the field is highest at the gate
edge where breakdown occurs. In this particular example, with a surface potential of 0.65 V, the field at the gate edge is reduced, thereby increasing the breakdown voltage. Using a one-dimensional analysis, the field at the gate edge can be shown to be:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/VBD_Surface_Traps.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cxi%28L%29%20%3D%20%5Cfrac%7BqN_D%7D%7B%5Cepsilon_s%7D%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%7D%7BqN_D%7D%28%5Cpsi_%7Bbi%7D&plus;V_D-V_G%29-%5Cfrac%7BN_%7Bst%7D%27%7D%7BN_D%7DL_%7BGD%7D%5E2%7D)

where N<sub>st</sub>' is the surface-trap density. Since GaAs lacks a common passivation layer such as SiO, for silicon, the breakdown in GaAs MESFETs are less controllable and have different breakdown behavior compared to Si JFETs.

One factor for a reduced breakdown voltage in MESFETs is due to tunneling current associated with the Schottky-barrier gate contact. At high fields, this tunneling current is from thermionic-field emission which has a temperature dependence. The gate current can initiate avalanche multiplication and induces lower drain breakdown voltage. Another factor is that GaAs MESFETs usually have higher current and transconductance than Si devices due to higher mobility. The higher channel current can initiate avalanche at a lower voltage, or produce the temperature effects which trigger earlier breakdown as discussed.

The breakdown voltage can be improved by extending the region between the gate and the drain. Furthermore, to maximize its function, the field distribution
should be made as uniform as possible. One technique is to introduce a doping gradient in the lateral direction. Another, called RESURF (reduced surface field) is to have a p-layer underneath such that at high drain bias, this n-layer is fully depleted.

### Arbitrary Doping and Enhancement Mode
Arbitrary Doping Profile. For an arbitrary doping profile in the channel region, the net potential variation inside the depletion width is related to the doping. In the linear region, where the drift velocity is always in the constant-mobility regime due to the small field or drain bias, the ID of JFET with any arbitrary doping is deriven as the form of:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDlin%7D%20%3D%20%5Cfrac%7BZ%5Cmu%7D%7BL%7D%5BQ%28a%29-Q%28W_%7BDs%7D%29%5DV_D)

In the saturation region, we first consider the case where saturation is caused by pinch-off (WDd = a) as opposed to velocity saturation. In this case, the ID and gm are given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZ%5Cmu%20q%7D%7B%5Cepsilon_sL%7D%5Cint_%7BW_%7BDs%7D%7D%5E%7Ba%7D%5BQ%28a%29-Q%28W_%7BD%7D%29%5DW_DN_DdW_D%20%5C%5C%5C%5C%5C%5C%20g_m%20%3D%20%5Cfrac%7BZ%5Cmu%7D%7BL%7D%5BQ%28a%29-Q%28W_%7BDs%7D%29%5D)

which shows that g, is equal to the conductance of the rectangular section of the semiconductor extending from y = WDs to a. For short-channel devices where velocity saturation determines current saturation, the drain current and gm are simply given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20Z%5Cnu_s%5BQ%28a%29-Q%28W_%7BDs%7D%29%5D%20%5C%5C%5C%5C%5C%5C%20g_m%20%3D%20%5Cfrac%7BZ%5Cnu_s%5Cepsilon_s%7D%7BW_%7BDs%7D%7D)

In real applications, it is often preferable to have good linearity, i.e., constant gm, meaning IDsat changes linearly with VG. Linearity of the transfer characteristics is approached by those profiles in which the depletion depth WD(VG) changes very little as a function of the gate voltage. The transfer characteristics for various doping profiles are shown in the following Fig. Note that both types of nonuniform dopings achieve linearity as the appropriate variable parameter is taken to its limit, which has a delta doping at x = a. The results shown are quite different from the constant-mobility case,
in which the doping profile has little effect on the transfer characteristics. Although the above equation implies a reduction of gm for lower gate voltage, the important quantity gm/C<sub>GS</sub> remains unaffected, where , C<sub>GS</sub> is the gate-source capacitance. This is because C<sub>GS</sub> = ε<sub>s</sub>/WDs and the above equation gives:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/ID_Doping.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bg_m%7D%7BC_%7BGS%7D%7D%20%3D%20Z%5Cnu_s%20%3D%20constant)

Experimental results have confirmed that FETs with graded channel doping or step dopings have improved linearity.

Enhancement-Mode Devices ===> Buried-channel FETs are usually normally-on devices. The basic current-voltage characteristics of normally-on and normally-off devices are similar, except for the value of the threshold voltage. For high-speed low-power applications, the normally-off (or enhancement-mode) device is very attractive. A normally-off device is one that does not have a conductive channel at VG = 0; that is, the built-in potential ψ<sub>bi</sub> of the gate junction is suficient to totally deplete the channel region. Mathematically, normally-off device has a positive VT:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_%7Bbi%7D%20%3E%20%5Cpsi_%7BP%7D%20%3E%20%5Cfrac%7BqN_Da%5E2%7D%7B2%5Cepsilon_s%7D)

### Microwave Performance
Small-Signal Equivalent Circuit ===> Field-effect transistors, especially GaAs MESFETs, are useful for low-noise amplification, high-efficiency power generation, and high-speed logic applications. We shall first consider the small-signal equivalent circuit of a MESFET or JFET. A small-signal lumped-element circuit for operation in the saturation region in common-source configuration is shown in the follwing Fig.

![]()
