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

For deriving general I-V characteristic of JFET or MESFET, we assume that: 1) Channel doping is uniform; 2) The gradual-channel approximation is valid (??<sub>x</sub> << ??<sub>y</sub>); 3) The depletion laye is abrupt; 4) The current gate is niglegeble. We start with the channel charge distribution which is related to the channel dimensions. The channel dimensions and its potential distributions under both gate and drain biases are shown in more details in the following Fig. 

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/JFET_Band_Diagram.png)

Channel-Charge Distribution ===> For a uniformly doped n-channel, under the gradual-channel approximation, the depletion-layer width W, varies only gradually along the channel (x-direction), and one can solve the one-dimensional Poisson equation in the y-direction:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bd%5Cxi_y%7D%7Bdy%7D%20%3D%20-%5Cfrac%7Bd%5E2%5CDelta%20%5Cpsi_i%7D%7Bdy%5E2%7D%20%3D%20%5Cfrac%7BqN_D%7D%7B%5Cepsilon_s%7D%20%5C%5C%5C%5C%5C%5C%20W_D%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D%20&plus;%20%5CDelta%20%5Cpsi_i%28x%29%20-%20V_G%29%7D%7BqN_D%7D%7D%20%5C%5C%5C%5C%5C%5C%20%5Cpsi_%7Bbi%7D%20%5Capprox%20%5Cfrac%7B1%7D%7Bq%7D%5BE_g%20-%20kTln%28%5Cfrac%7BN_C%7D%7BN_D%7D%29%5D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20for%5C%3BJFET%20%5C%5C%5C%5C%5C%5C%20%5Cpsi_%7Bbi%7D%20%3D%20%5Cphi_%7BBn%7D%20-%20%5Cfrac%7BkT%7D%7Bq%7Dln%28%5Cfrac%7BN_C%7D%7BN_D%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20for%5C%3BMESFET)

The potential difference ????<sub>i</sub>(x) is the potential of the neutral channel [- E<sub>i</sub>(x)/q] with respect to the source. So at the drain end, ????<sub>i</sub>(L) = V<sub>D</sub>. The depletion widths at the source and drain ends are given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20W_%7BDs%7D%20%3D%20W_D%280%29%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D%20-%20V_G%29%7D%7BqN_D%7D%7D%20%5C%5C%5C%5C%5C%5C%20W_%7BDd%7D%20%3D%20W_D%28L%29%20%3D%20%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D%20&plus;V_D%20-%20V_G%29%7D%7BqN_D%7D%7D)

The maximum value of gate bias applied to increase the current is limited to V<sub>G</sub> = ??<sub>bi</sub> which corresponds to the condition of W<sub>Ds</sub> = 0. This flat-band condition in practice is not achievable due to the excessive forward current of the gate junction. The maximum value of W<sub>Dd</sub> is equal to a, and the corresponding total band bending is called the pinch-offpotential, defined as: 

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_P%20%5Cequiv%20%5Cfrac%7BqN_Da%5E2%7D%7B2%5Cepsilon_s%7D)

The channel charge density, which is responsible for the current conduction, is proportional to the net channel opening, given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_n%28x%29%20%3D%20qN_D%28a-W_D%28x%29%29%20%5C%5C%5C%5C%20I_D%28x%29%20%3D%20ZQ_n%28x%29%5Cnu%28x%29%20%5C%5C%5C%5C%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7DQ_n%28x%29%5Cnu%28x%29dx%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%281%29)

Equation 1 requires knowledge of the carrier velocity under an applied field, so the ??-?? relationship is critical. we find that current saturation can
originate from two very different mechanisms. The first is due to channel pinch-off when the net channel is totally pinched off by the depletion width. This is called long-channel behavior, and found to be modelled well simply by a constant mobility. The second possible mechanism, especially true for short-channel devices, is that the field is high enough such that mobility is no longer constant and eventual the velocity rises to a constant value called saturation velocity. This occurs before the channel is pinched off.

Constant Mobility ===> With constant mobility and ??(x)=d????<sub>i</sub>(x)/dx the following equation is obtained for I<sub>D</sub> in different regiems:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20G_i%5C%7B%7BV_D%20-%20%5Cfrac%7B2%7D%7B3%20%5Csqrt%7B%5Cpsi_P%7D%7D%5B%28%5Cpsi_%7Bbi%7D&plus;V_D-V_G%29%5E%7B3/2%7D-%28%5Cpsi_%7Bbi%7D-V_G%29%5E%7B3/2%7D%5D%7D%5C%7D%20%5C%5C%5C%5C%5C%5C%20G_i%20%3D%20%5Cfrac%7BZq%5Cmu%20N_Da%7D%7BL%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%282%29)

where G<sub>i</sub> is the full channel conductance when W<sub>D</sub> = 0. In the linear region, VD << VG and VD << ??<sub>bi</sub>, above equation is reduced to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDlin%7D%20%3D%20G_i%281-%5Csqrt%7B%5Cfrac%7B%5Cpsi_%7Bbi%7D-V_G%7D%7B%5Cpsi_P%7D%7D%29V_D%20%5C%5C%5C%5C%5C%5C%20I_%7BDlin%7D%20%3D%20%5Cfrac%7BG_i%7D%7B2%5Cpsi_P%7D%28V_G-V_T%29V_D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%20%5Capprox%20V_T%20%5C%5C%5C%5C%5C%5C%20V_T%20%3D%20%5Cpsi_%7Bbi%7D%20-%20%5Cpsi_P)

When the drain bias continues to increase, the current according to Eq. 2 goes through the nonlinear region. It reaches a peak and actually drops beyond that point. The drop of current is not physical, but it corresponds to a pinch-off condition when W<sub>Dd</sub> = a. The V<sub>D</sub> at the onset of this condition can be shown to occur at:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_%7BDsat%7D%20%3D%20%5Cpsi_P%20-%20%5Cpsi_%7Bbi%7D%20&plus;%20V_G%20%3D%20V_G%20-%20V_T%20%5C%5C%5C%5C%20I_%7BDsat%7D%20%3D%20G_i%5B%5Cfrac%7B%5Cpsi_P%7D%7B3%7D%20-%20%28%5Cpsi_%7Bbi%7D-V_G%29%281-%5Cfrac%7B2%7D%7B3%7D%5Csqrt%7B%5Cfrac%7B%5Cpsi_%7Bbi%7D-V_G%7D%7B%5Cpsi_P%7D%7D%29%5D%20%5C%5C%5C%5C%5C%5C%20g_m%20%5Cequiv%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20G_i%281-%5Csqrt%7B%5Cfrac%7B%5Cpsi_%7Bbi%7D-V_G%7D%7B%5Cpsi_P%7D%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%283%29)

Qualitatively, for drain bias higher than VDsat, the pinch-off point starts to migrate toward the source. However, the potential at the pinch-off point remains to be VDsat, independent of VD. The field within the drift region thus remains fairly constant, giving rise to current saturation. Practical devices show that IDsat does not saturate completely with VD. This is due to the reduction in the effective channel length, which is measured between the source and the pinch-off point. Equation 17 can also be simplified using Taylor's expansion around VG = VT:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%5Capprox%20%5Cfrac%7BG_i%7D%7B4%5Cpsi_P%7D%28V_G-V_T%29%5E2%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%20%5Capprox%20V_T%20%5C%5C%5C%5C%5C%5C%20g_m%20%3D%20%5Cfrac%7BG_i%7D%7B2%5Cpsi_P%7D%28V_G-V_T%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20V_G%20%5Capprox%20V_T)

It is seen here that the forms of above equations are similar to that of MOSFET only near the threshold, i.e., VG = VT. This stems from the fact that the gate capacitance (or depletion width) is gate-bias dependent in JFET and MESFET, while that in the MOSFET (gate dielectric) is fixed. In other words, in a MOSFET the channel charge is linearly dependent on VG, while that is not true for a JFET or MESFET. 

Velocity-Field Relationship ===> For long-channel devices, the field is low enough that the carrier velocity is treated as being proportional to the field, i.e., constant mobility. For FETs with short channels, significant discrepancies are encountered between experiment and basic theory. One main reason for the discrepancies is the higher internal field for short channels. The following figure shows the qualitative dependence of the drift velocity versus electric field for silicon. At low fields the drift velocity increases linearly with the field, and the slope corresponds to a constant mobility. At higher fields, the carrier velocity deviates from a linear dependence. It becomes lower than simple extrapolation from the low-field slope, and eventually saturates to a value called saturation velocity ??s. So for short-channel devices, these effects have to be taken into account. For silicon the drift velocity approaches its saturation value of lE7 cm/s at fields above 5E4 V/cm. For some semiconductors such as GaAs and InP, the drift velocity first reaches a peak value and then decreases toward a saturation velocity.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Drift_Velocity_E.png)

In this section, we will examine two simple u-E relationships. The first is the two-piece linear approximation shown in the above figure. The second is an empirical formula which has a smooth transition between the constant-mobility regime to the saturation-velocity regime, given as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cnu%28%5Cxi_x%29%20%3D%20%5Cfrac%7B%5Cmu%5Cxi_x%7D%7B1&plus;%28%5Cmu%5Cxi_x/%5Cnu_s%29%7D%20%3D%20%5Cfrac%7B%5Cmu%5Cxi_x%7D%7B1&plus;%28%5Cxi_x/%5Cxi_c%29%7D)

As seen, both relationships contain an important parameter, the critical field ??<sub>c</sub>

Field-Dependent Mobility: Two-Piece Linear Approximation ===> We first discuss velocity saturation based on the two-piece linear approximation. Note that in this model, the constant-mobility results (i.e., Eq. 2) are valid up to the point where the maximum field, which is at the drain end, reaches the critical field. Once at that VDsat, which is lower than the VDsat of the constant-mobility model, the current saturates at a new and lowered IDsat. So the main task is to calculate this new VDsat. We start with Eq. 1 (and substitute ?? = ???? ) which contains the relationship between field and current. Setting ??=??<sub>c</sub> and ID=IDsat, we have:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20Zq%5Cmu%20N_D%20%5Cxi%20_c%5Ba-%5Csqrt%7B%5Cfrac%7B2%5Cepsilon_s%28%5Cpsi_%7Bbi%7D&plus;V_%7BDsat%7D-V_G%29%7D%7BqN_D%7D%7D%5D%20%5C%5C%5C%5C%5C%5C%20%5Cxi_cL%20%3D%20%5Cfrac%7BV_%7BDsat%7D%20-%20%5B2/%283%5Csqrt%7B%5Cpsi_P%7D%29%5D%5B%28%5Cpsi_%7Bbi%7D&plus;V_%7BDsat%7D-V_G%29%5E%7B3/2%7D-%28%5Cpsi_%7Bbi%7D-V_G%29%5E%7B3/2%7D%5D%7D%7B1-%5Csqrt%7B%28%5Cpsi_%7Bbi%7D&plus;V_%7BDsat%7D-V_G%29/%5Cpsi_P%7D%7D)

Visual examination of this equation indicates that current saturates as VD approaches ??<sub>c</sub>L , or VD/L ??? ??<sub>c</sub>. Once VDsat is known, IDsat can be calculated from Eq. 2 of the constant-mobility model. One also finds that since VDsat is lower than the value from the constant-mobility model, current saturation occurs before the channel is pinched off.

Field-Dependent Mobility: Empirical Formula ===> We next derive the current equation based on the empirical formula given in the above. Substituting this into Eq. 1 and integrating from x = 0 to L , we obtain:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20%5Cfrac%7BG_i%7D%7B1&plus;%28V_D/%5Cxi_cL%29%7D%5C%7B%7BV_D%20-%20%5Cfrac%7B2%7D%7B3%20%5Csqrt%7B%5Cpsi_P%7D%7D%5B%28%5Cpsi_%7Bbi%7D&plus;V_D-V_G%29%5E%7B3/2%7D-%28%5Cpsi_%7Bbi%7D-V_G%29%5E%7B3/2%7D%5D%7D%5C%7D)

Comparing this to Eq. 2, this new result gives a current that is reduced by a factor of (1 + VD/??<sub>c</sub>L) from that of the constant-mobility model. In order to obtain VDsat, we seek the current peak from the above equation by setting dID/dVD = 0. This yields a transcendental equation for VDsat. Solutions of VDsat have been calculated and plotted in the following Fig., for various values of ??<sub>c</sub>L. The top curve (??<sub>c</sub>L = ???) becomes the limit of the constant-mobility model. Note that with decreasing ??<sub>c</sub>L the saturation of drain current is reached at smaller values of drain voltage.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/VDsat_Psi.png)

Having gone through the three models of u - 8 relationships, it is informative to compare their results on the I-V characteristics. Here we use an example of one I-V curve for a fixed VG (=0) , and the other parameters are; ??P = 4V, ??bi = 1V, and ??<sub>c</sub>L = 2V. The results are shown in the following fig. The values of the VDsat for the constant mobility, two-piece liner approximation, and the empirical formula are 3V, 1.3V, and 1.9 V respectively. Note that the curve for the two-piece-linear model lies on the constant-mobility curve until VDsat. The lowest current of the three curves corresponds to the empirical formula of Eq. 29 since at any field, the velocity is the lowest among the three models as shown in Fig. 4.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Constant_Peice_Emprical.png)

Velocity Saturation ===> One limiting case is the saturation-velocity model which is expected to be valid in the limit of very short gates where L << VD/??<sub>c</sub>. In this assumption, the carriers travel with us in the whole region under the gate, and are totally independent of the low-field mobility. Starting from Eq. 1, the saturation current is simply given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20ZQ_n%5Cnu_s%20%3D%20Zq%28a-W_%7BDs%7D%29N_D%5Cnu_s)

which is reduced from that of the constant-mobility model given by G<sub>i</sub>??<sub>P</sub>/3. The choice of depletion width at the source WDs, rather than at the drain is apparent as we discuss details of the carrier-density and velocity profiles in the next section (Dipole-Layer Formation). This equation shows an interesting feature that the saturation current is now totally independent of the channel length. The transconductance is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20-ZqN_D%5Cnu_s%5Cfrac%7BdW_%7BDs%7D%7D%7BdV_G%7D%20%3D%20%5Cfrac%7BZ%5Cepsilon_s%5Cnu_s%7D%7BW_%7BDs%7D%7D)

Since ??<sub>s</sub>/WDS is the gate-source capacitance C<sub>GS</sub> this equation reduces to the familiar FET equation:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_m%20%3D%20ZC_%7BGS%7D%5Cnu%20_s)

This equation also has the interesting feature that gm is constant and totally independent of gate bias as well as channel length. Olutput characteristics of constant mobility and velocity saturation are compared in the following Fig. Note that the saturation current and saturation voltage are lower under velocity saturation, but the linear regions remain similar. The constant gm under velocity saturation is indicated by the equal spacing of the I-V curves under different VG. As shown, this velocity-saturation limit provides very simple derivations and results, thus giving a good insight of the short-channel
limit. In fact, the simple formulae can fit quite well to the state-of-the-art short channel devices.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Constant_Saturation.png)

Even though velocity saturation sets a limit on the maximum carrier speed in a field-effect transistor, there are two special effects that enable higher speed at part of the channel where the local field is high. The first is related to the material properties, such as in GaAs and InP, which display a transferred-electron effect. At moderately high fields, the drift velocity is actually higher than the saturation velocity. To include this negative-
resistance effect in modeling the I- V characteristics analytically would be very difficult. The second effect is present in ultra-short devices when their channel lengths are comparable to or smaller than the mean free path of scattering. For very short gates, the electrons may not have enough time or distance to reach equilibrium transport in the high-field region of the channel. In such cases, the electrons enter the high-field region and are accelerated to a higher velocity before relaxing to the equilibrium value. Carriers can thus overshoot to more than twice the steady-state velocity and then relax to the equilibrium condition after traveling a certain distance. The overshoot will shorten the electron transit time. This overshoot is expected to improve high-frequency response, especially for the GaAs FET. This phenomenon is related indirectly to low-field mobility since they are both determined by scattering. A material with higher mobility can have more ballistic effect for the same channel length.

Dipole-Layer Formation ===> Below the saturation drain bias VDsat, the potential along the channel increases from zero at the source to VD at the drain. Thus, the gate contact becomes increasingly reverse-biased with respect to the channel, and the depletion width becomes wider as we proceed from source to drain. The resulting decrease in channel opening b must be compensated by an increase in electric field and electron velocity to maintain a constant current throughout the channel. As VD is increased further to VDsat, the electrons reach the saturation velocity at the drain end of the gate (following fig a). The channel is constricted to the smallest cross section b1 under the gate. The electric field reaches the critical value ??<sub>c</sub> at this point, and , ID starts to saturate. The electron density n(x), however, remains equal to the doping density ND as long as the field does not exceed the critical value ??<sub>c</sub>. The condition of VD > VDsat is displayed in the following Fig. b. The saturation current is given by:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Dipole_Layer.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20Zq%5Cnu_sn%28x%29b%28x%29)

If the drain voltage is increased beyond VDsat, the depletion region widens toward the drain. The point x1, where the electrons reach the saturation velocity and the channel width is b1, moves toward the source. Note that there are three locations of interest; x1 and x2 are locations where the channel opening is b1, and x1 and x3 are locations where ??=??<sub>c</sub>. This also means that in the region x1 to x2 the channel is narrower than b1, and in the region x1 to x3, carriers travel with ??<sub>s</sub>. Since the velocity is saturated, in the region x1 to x2 the change in channel width must be compensated by a change in carrier density to maintain constant current. According to the above Eq., an electron accumulation layer (n > ND) must form in this region, where the channel opening is smaller than b1. At x2 the channel opening is again b1, and the negative space charge changes to a positive space charge (n < ND) to preserve constant current. Between x1 and x3 the electron velocity remains saturated but the channel width is larger than b1. So by virtue of the same above Eq., carrier concentration is lower than ND in order to keep the saturation current constant. Therefore, the drain voltage applied in excess of VDsat forms a dipole layer in a channel that extends beyond the drain end of the gate.

Breakdown ===> For drain voltages beyond VDsat, the drain current is assumed to remain essentially the same as the saturation current. As the drain voltage increases further, breakdown occurs where the current rises sharply with the drain bias. This breakdown occurs at the gate edge toward the drain side where the field is the highest. The fundamental mechanism responsible for breakdown is impact ionization. Since impact ionization is a strong function of the electric field, the maximum field is often regarded as the first-order criterion for breakdown. Using a simple one-dimensional analysis in the x-direction, and treating the gate-drain structure as a reverse-biased diode, the drain breakdown voltage VDB is similar to that of the gate-junction breakdown and is linearly dependent on the relative voltage of the drain to the gate V<sub>BD</sub> = V<sub>B</sub> - V<sub>G</sub>, where V<sub>B</sub> the breakdown voltage of the gate diode and is a function of channel doping level, among other factors. The general breakdown behavior of the mentioned equation is shown in the following Fig. It is shown that for higher VG, the drain breakdown voltage becomes higher by the same amount. Such characteristics general hold true for silicon JFETs. But for MESFETs on GaAs, the breakdown mechanisms are much more complicated. They generally have lower breakdown values and the dependence of VG no longer follows. 

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/VBD_VG.png)

Unlike a MOSFET where the heavily doped source and drain overlap the gate at the gate edges, the JFETs and MESFETs have a gap between the gate and the
source/drain contacts (or heavily doped regions under the contacts). For breakdown consideration, this gate-drain distance L<sub>GD</sub> is critical. In this gap the doping level is the same as the channel. If surface traps are present in this gate-drain spacing, they can deplete part of the channel doping and affect the field distribution. In certain cases they can improve the breakdown voltage. Two-dimensional simulations in the following fig displays the field distribution as a function of surface potential created by surface traps. Without surface traps (??<sub>s</sub> = 0), the field is highest at the gate
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
in which the doping profile has little effect on the transfer characteristics. Although the above equation implies a reduction of gm for lower gate voltage, the important quantity gm/C<sub>GS</sub> remains unaffected, where , C<sub>GS</sub> is the gate-source capacitance. This is because C<sub>GS</sub> = ??<sub>s</sub>/WDs and the above equation gives:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/ID_Doping.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cfrac%7Bg_m%7D%7BC_%7BGS%7D%7D%20%3D%20Z%5Cnu_s%20%3D%20constant)

Experimental results have confirmed that FETs with graded channel doping or step dopings have improved linearity.

Enhancement-Mode Devices ===> Buried-channel FETs are usually normally-on devices. The basic current-voltage characteristics of normally-on and normally-off devices are similar, except for the value of the threshold voltage. For high-speed low-power applications, the normally-off (or enhancement-mode) device is very attractive. A normally-off device is one that does not have a conductive channel at VG = 0; that is, the built-in potential ??<sub>bi</sub> of the gate junction is suficient to totally deplete the channel region. Mathematically, normally-off device has a positive VT:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_%7Bbi%7D%20%3E%20%5Cpsi_%7BP%7D%20%3E%20%5Cfrac%7BqN_Da%5E2%7D%7B2%5Cepsilon_s%7D)

### Microwave Performance
Small-Signal Equivalent Circuit ===> Field-effect transistors, especially GaAs MESFETs, are useful for low-noise amplification, high-efficiency power generation, and high-speed logic applications. We shall first consider the small-signal equivalent circuit of a MESFET or JFET. A small-signal lumped-element circuit for operation in the saturation region in common-source configuration is shown in the follwing Fig.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Microwave_Equi_Circuit.png)

In the intrisic FET, the elements C<sub>GS</sub>'+C<sub>GD</sub>' are the total gate-channel capacitance (= C<sub>G</sub>'). R<sub>ch</sub> is the channel resistance; R<sub>DS</sub> is the output resistance which reflects the nonsaturating drain current with drain bias. The extrinsic (parasitic) elements include the source and drain series resistances R<sub>S</sub> and R<sub>D</sub>, the gate resistance R<sub>G</sub>, the parasitic input capacitance C<sub>par</sub>' and output (drain-source) capacitance C<sub>DS</sub>'. The leakage current in the gate-to-channel junction can be expressed as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_G%20%3D%20I_0%5Bexp%28%5Cfrac%7BqV_G%7D%7BnkT%7D%29%20-%201%5D)

where n is the diode ideality factor (1 < n < 2) and I0 is the saturation current. The input resistance is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20R_%7Bin%7D%20%5Cequiv%20%28%5Cfrac%7BdI_G%7D%7BdV_G%7D%29%5E%7B-1%7D%20%3D%20%5Cfrac%7BnkT%7D%7Bq%28I_0&plus;I_G%29%7D)

As I, approaches zero, the input resistance at room temperature is about 250 MR for I<sub>G</sub> = 1E-10 A. It becomes even higher for negative gate bias (negative VG). The FET obviously has a very high input resistance, even though it is not as ideal as in a MOSFET which has an insulating gate.

The source and drain series resistances, which cannot be modulated by the gate voltage, will introduce an IR drop between the gate and the source and drain contacts. These IR drops will reduce the drain conductance as well as the transconductance. The internal effective voltages VD and VG should then be replaced by [V<sub>D</sub>-I<sub>D</sub>(R<sub>S</sub>+R<sub>D</sub>)] and (V<sub>G</sub> - IR<sub>S</sub>), respectively. In the linear region, the resistances R<sub>S</sub> and R<sub>D</sub> are in series, adding to the total measured drain-source resistance (R<sub>S</sub>+R<sub>D</sub>+R<sub>ch</sub>). In the saturation region, the drain resistance R<sub>D</sub> will cause an increase of the drain voltage at which current saturation occurs. Beyond that voltage V<sub>D</sub> > V<sub>Dsat</sub>, the magnitude of V<sub>D</sub> has no effect on the drain current. By the same token, the measured transconductance in the saturation region is affected only by the source resistance. Thus R<sub>D</sub> has no further effect on gm, and the measured extrinsic transconductance is equal to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20g_%7Bmx%7D%20%3D%20%5Cfrac%7Bg_m%7D%7B1&plus;R_Sg_m%7D)

Cutoff Frequency ===> For a measure of the high-speed capability, the cutoff frequency f<sub>T</sub> and the maximum frequency of oscillation f<sub>max</sub> are commonly used. The f<sub>T</sub> is defined as the frequency of unity gain, at which the small-signal input gate current is equal to the drain current of the intrinsic FET. The f<sub>max</sub> is the maximum frequency at which the device can provide power gain. The f<sub>T</sub> is a more appropriate figure-of-merit for digital circuits where speed is the primary concern, and f<sub>max</sub> is more relevant for analog-circuit applications.

Based on unity gain, one can use the derivation discussed in Section 5.3.1 for an expression:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20f_T%20%3D%20%5Cfrac%7Bg_m%7D%7B2%5Cpi%20C_%7Bin%7D%27%7D%20%3D%20%5Cfrac%7Bg_m%7D%7B2%5Cpi%20%28C_%7BG%7D%27&plus;C_%7Bpar%7D%27%29%7D)

Here C<sub>in</sub>' is the total input capacitance, and C<sub>G</sub>' is the sum of C<sub>GS</sub>' and C<sub>GD</sub>'. For an ideal case of zero input parasitics ( C<sub>par</sub>' = 0), we obtain:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20f_T%20%3D%20%5Cfrac%7Bg_m%7D%7B2%5Cpi%20C_%7BG%7D%27%7D%20%3D%20%5Cfrac%7B%5Cnu%7D%7B2%5Cpi%20L%7D)

This equation has the physical meaning that f<sub>T</sub> is related to the ratio L/?? which happens to be the transit time for a carrier to travel from source to drain. The drift velocity ?? is equal to the saturation velocity ??<sub>s</sub> for short channels, and for a 1-um gate length, the transit time is of the order of 10 ps. In practice, the parasitic input capacitance C<sub>par</sub>' is a fraction of C<sub>G</sub>', so f<sub>T</sub> is slightly below its theoretical maximum value.

The speed limitations of FETs are also dependent on device geometry and material properties. In the device geometry, the most-important parameter is the gate length L. Decreasing L will decrease the total gate capacitance [ C<sub>G</sub>' ??? (Z x L )] and increase the transconductance (before velocity saturation); consequently, f<sub>T</sub> improves. As for the carrier transport, since the internal field varies in magnitude along the channel, drift velocities in all field strength are critical. These include the low-field mobility, saturation velocity in high field, and for some materials, peak velocity in medium field in the presence of the transferred-electron effect. In Si and GaAs, electrons have a higher low-field mobility than holes have. Therefore only n-channel FETs are used in microwave applications. The low-field mobility in GaAs is about five times higher than that of silicon, therefore the frequency f<sub>T</sub> is expected to be higher in GaAs. For the same gate length, InP is expected to have even higher f<sub>T</sub> than GaAs because of its higher peak velocity. In any case, for these materials, FETs with gate lengths 0.5 pm or less will have f<sub>T</sub> in excess of 30 GHz.

Maximum Frequency of Oscillation ===> The f<sub>max</sub> is defined as the frequency at which the unilateral gain is unity. For the small input-to-output resistance ratio r<sub>1</sub>, f<sub>max</sub> is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20f_%7Bmax%7D%20%5Capprox%20%5Csqrt%7B%5Cfrac%7Bf_T%7D%7B8%5Cpi%20R_G%20C_%7BGD%7D%27%7D%7D%20%5C%5C%5C%5C%5C%5C%20r_1%20%5Cequiv%20%5Cfrac%7BR_G&plus;R_%7Bch%7D&plus;R_S%7D%7BR_%7BDS%7D%7D)

At f<sub>max</sub>, unity power gain is reached. To maximize f<sub>max</sub> the frequency f<sub>T</sub> and the resistance ratio R<sub>ch</sub>/R<sub>DS</sub> must be optimized in the intrinsic FET. In addition, the extrinsic resistances R<sub>G</sub> and R<sub>S</sub> and the feedback capacitance C<sub>GD</sub>' must also be minimized.

Power-Frequency Limitations ===> For power applications, both high voltage and high current are required. These, however, demand device designs that are in conflict with one another, and in addition, they also compromise the speed, so a trade-off has to be considered. For high current, the total channel dose (N<sub>D</sub>xa) has to be high. To maintain high breakdown voltage, N<sub>D</sub> cannot be too high and L cannot be too small. For a high f<sub>T</sub>, L has to be minimized and as a consequence, N<sub>D</sub> has to increase. The last constraint comes about because of the following.

For a gate electrode to have adequate control of the current transport across the channel, the gate length must be somewhat larger than the channel depth, that is L/a > ??. So to reduce L, the channel depth a has to be reduced at the same time, which implies a higher doping level to maintain a reasonable current. Because of this, some scaling rules have been proposed. These include constant LN<sub>D</sub> scaling, constant L<sup>1/2</sup>N<sub>D</sub>
scaling, and constant L<sup>2</sup>N<sub>D</sub> scalling. In practical Si and GaAs MESFETs, the highest doping level is about 5E17 /cm3 because of breakdown phenomena. Using the simple velocity-saturation estimate of I<sub>Dsat</sub>/Z = qN<sub>D</sub>????<sub>s</sub>, and ??<sub>s</sub> of 1E7 cm/s , to
maintain a current of 3 A/cm, this doping level limits the minimum gate length to about 0.1 pm, with a corresponding maximum f<sub>T</sub> of the order of 100 GHz.

In high-power operation, the device temperature increases. This increase causes a reduction of the mobility and saturation velocity, since the mobility varies as [T(K)]<sup>-2</sup> and velocity as [T(K)]<sup>-1</sup>. Therefore, the FET has negative temperature coefficient and will be thermally stable under high-power operation.

The state-of-the-art power-frequency performance of GaAs FETs is shown in the following Fig. A higher frequency range can be reached with MODFETs, at the expense of lower power. With further miniaturization to submicron dimensions, and with improved designs and reduction of parasitics, FETs of higher powers operated at higher frequencies can be made. Also with semiconductor materials of higher band-gaps such as Sic and GaN, the curve can be shifted upward. For GaN devices, the curve can be higher by more than tenfold in power.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/High_Power_Frequency.png)

Noise Behavior ===> The MESFET and JFET are low-noise devices, because only majority carriers participate in their operations, and these carriers transport through the channel in the bulk and free of surface or interface scattering. However, in practical devices, extrinsic resistances are unavoidable, and these parasitic resistances are mainly responsible for the noise behavior.

The equivalent circuit used for noise analysis is shown in in the following Fig. Noise sources i<sub>ng</sub>, i<sub>nd</sub>, e<sub>ng</sub>, and e<sub>ns</sub> represent the induced gate noise, induced drain noise, thermal noises of the gate resistance R<sub>G</sub> and source resistance R<sub>S</sub>, respectively. The e<sub>s</sub> and Z<sub>s</sub> are the signal source voltage and source impedance. The circuit within the dashed
lines corresponds to the intrinsic FET. 

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Noise_equivalent.png)

The noise figure is defined as the ratio of the total noise power to the noise power generated from the source impedance alone. So the noise figure depends also on the circuitry external to the device. There is an important parameter called the minimum noisefigure which is obtained with both the source impedance and load impedance being optimized for noise performance. This minimum noise figure for a practical device has been obtained from the equivalent
circuit to be:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20f_%7Bmin%7D%20%5Capprox%201%20&plus;%202%20%5Cpi%20C_1fC_%7BGS%7D%27%5Csqrt%7B%5Cfrac%7BR_G&plus;R_S%7D%7Bg_m%7D%7D)

where C1 is a constant of value 2.5 s/F. Clearly for low-noise performance, one should minimize the parasitic gate resistance and source resistance. At a given frequency, the noise decreases with decreasing gate length (C<sub>GS</sub>' ??? Z x L). We should be reminded that RG and gm are proportional to the device width Z, while Rs is inversely proportional to Z. This leads to decreasing noise with decreasing channel width. The graded-channel FET (Fig. 11) has been found to yield less noise (1 to 3 dB lower) than uniformly doped devices having the same geometry. This difference in noise is related to gm. The reduction of gm for a graded-channel FET gives superior noise performance.

### Device Structure
The schematic diagrams of high-performance MESFETs are shown in the following Fig. The MESFET structures fall into two major categories: the ion-implanted planar structure and the recessed-channel (or recessed-gate) structure. All devices have a semiinsulating (SI) substrate for compound semiconductors such as GaAs.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/MESFET_Structure.png)

In the ion-implanted planar process (Fig. a), the active region is created by ion implantation to over-compensate the deep-level impurities in the SI-substrate. Naturally the active device is isolated vertically and horizontally by the semiinsulating material. To minimize the source and drain parasitic resistance, the deeper n+-implantations should be as close to the gate as possible. This is done by various self-aligned processes. In a gate-priority self-aligned process, the gate is formed first, and the source/drain ion implantation is self-aligned to the gate. In this process, since ion implantation requires high-temperature anneal for activation, the gate has to made of materials that can withstand high-temperature processing. Examples are Ti-W alloy,
WSi2, and TaSi2. The second approach is ohmic-priority where the source/drain implantation and anneal are done before the gate formation. Such process relaxes the previous requirement on the gate material.

In the recessed-channel process (Fig. b), the active layers are grown epitaxially over the SI-substrate. An intrinsic buffer layer is first grown and followed by an active channel layer. The buffer layer serves to eliminate defects duplicating from the semiinsulating substrate. Finally an epitaxial n+-layer is grown over the active n<sup>+</sup>-channel to reduce the source and drain contact resistance. This n<sup>+</sup>-layer is selectively removed in the region between the source and the drain for gate formation. One of the advantages of this recessed-channel structure is that the surface is further away from the n-channel layer so that surface effects such as transient response25 and other reliability problems are minimized. One disadvantage of this scheme is the additional steps required for isolation which could be a mesa etching process (as shown) or an isolation implantation that converts the semiconductor into high-resistivity material.

For superior microwave performance, the gate can be made into the shape of a T-gate or mushroom-gate as shown in the inset of Fig. 16. The shorter dimension at the bottom of the gate is the electrical channel length and it serves to optimize f<sub>T</sub> and g<sub>m</sub>, while the wider top portion reduces the gate resistance for an improved f<sub>max</sub> and noise figure.

The JFET structures are similar to those of the MESFET, with the additional step of ap-n junction formed underneath the gate contact by ion implantation. JFETs are more suitable for power applications and seldom used in state-of-the-art high-frequency applications. Part of the reason is that the channel length from ap-n junction is more different to control and miniaturize compared to a metal gate. One common inherent shortcoming of both the MESFET and JFET is that the heavily doped source and drain regions cannot overlap the gate as in the case of a MOSFET.

## MODFET
The modulation-doped field-effect transistor (MODFET) is also known as the high-electron-mobility transistor (HEMT), two-dimensional electron-gas field-effect transistor (TEGFET), and selectively doped heterojunction transistor (SDHT). Sometimes it is simply referred to by the generic name HFET (heterojunction field-effect transistor). The unique feature of the MODFET is the heterostructure, in which the wide-energy-gap material is doped and carriers diffuse to the undoped narrow-bandgap layer at which heterointerface the channel is formed. The net result of this modulation doping is that channel carriers in the undoped heterointerface are spatially separated from the doped region and have high mobilities because there is no impurity scattering. The development of MBE and MOCVD technologies in the 1970s made heterostructures, quantum wells, and superlattices practical and more accessible for MODFETs.

The main advantage of modulation doping is the superior mobility. This phenomenon is demonstrated in the following figure which compares mobilities in the bulk, relevant for MESFETs and JFETs, to that in the modulation-doped channel. It is seen here that since in a MESFET or JFET the channel has to be doped to a reasonably high level (> 1E17 /cm3), the modulation-doped channel has much higher mobilities at all temperatures. The modulation-doped channel does not suffer from impurity scattering which dominates at low temperatures. This benefit stems from the screening effect of a two-dimensional electron gas, where its conduction path is confined to a small cross-section which is smaller than 10 nm with high volume density.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/HEMT_JEFET_MESFET.png)

### Basic Device Structure
The most-common heterojunctions for the MODFETs are the AlGaAs/GaAs, AlGaAs/InGaAs, and InAlAs/InGaAs heterointerfaces. A basic MODFET structure based on the AlGaAs/GaAs system is shown in the following Fig. It is seen here that the barrier layer AlGaAs under the gate is doped, while the channel layer GaAs is undoped.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/MODFET.png)

This is the principle of modulation doping such that carriers from the doped barrier layer are transferred to reside at the heterointerface and are away from the doped region to avoid impurity scattering. The doped barrier layer is typically around 30-nm thick. Very often, a ??-doped charge sheet is used within the barrier layer and placed close to the channel interface, instead of uniform doping. The top layer of n<sup>+</sup>-GaAs is for better source and drain ohmic contacts. These contacts are made from alloys containing Ge, such as AuGe. Similar to MESFETs, the metal gate is sometimes made into the shape of a T-gate to reduce the gate resistance. Most MODFETs reported are n-channel devices for higher electron mobility.

### I-V Characteristics
Based on the principle of modulation doping, the impurities within the barrier layer are completely ionized and carriers depleted away. Referring to the energy-band diagrams of the following Fig., the potential variation within the depleted region is given by:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/MODFET_Band_Diagram.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_P%20%3D%20%5Cfrac%7Bq%7D%7B%5Cepsilon_s%7D%5Cint_0%5E%7By0%7D%20N_D%28y%29ydy)

for a general doping profile. For uniform doping, this built-in potential becomes:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_P%20%3D%20%5Cfrac%7BqN_Dy_0%5E2%7D%7B2%5Cepsilon_s%7D)

For a planar-doped charge sheet n<sub>sh</sub> located at a distance of y<sub>1</sub> from the gate, this expression yields:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cpsi_P%20%3D%20%5Cfrac%7Bqn_%7Bsh%7Dy_1%7D%7B%5Cepsilon_s%7D)

The advantage here, compared to the uniformly doped AlGaAs layer, is the reduction of traps that are believed to be responsible for the anomalous behavior of current collapse at low temperature. The close proximity of dopants to the channel also gives a lower threshold voltage.

Like any other field-effect transistor, an important parameter is the threshold voltage, the gate bias at which the channel starts to form between the source and drain. From the above Fig., first-order approximation shows that this occurs when the Fermi level E<sub>F</sub> at the GaAs surface coincides with the conduction-band edge E,. This corresponds to the bias condition of:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_T%20%5Capprox%20%5Cphi_%7BBn%7D%20-%20%5Cpsi_P%20-%20%5Cfrac%7B%5CDelta%20E_C%7D%7Bq%7D)

It can be seen here that by choosing the doping profile and barrier height, VT can be varied between positive and negative values. The example shown in the above Fig. has a positive VD and the transistor is called an enhancement-mode (normally-off) device, as opposed to a depletion-mode (normally-on) device. Once the threshold voltage is known, the rest of the analysis in deriving the I-V characteristics are similar to that for the MOSFETs. With gate voltage larger than the threshold voltage, the charge sheet in the channel induced by the gate is capacitively coupled and is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_n%20%3D%20C_o%28V_G%20-%20V_T%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20C_o%20%3D%20%5Cfrac%7B%5Cepsilon_s%7D%7By_0&plus;%5CDelta%20y%7D)

where ??y is the channel thickness of the two-dimensional electron gas, estimated to be around 8 nm. When a drain bias is applied, the channel has a variable potential with distance and its value with respect to the source is designated as ????(x). It varies along the channel from 0 at the source to V, at the drain. The channel charge as a function of position becomes:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20Q_n%20%3D%20C_o%28V_G%20-%20V_T%20-%20%5CDelta%20%5Cpsi%28x%29%29%20%5C%5C%5C%5C%20I_D%28x%29%20%3D%20ZQ_n%28x%29%5Cnu%28x%29%20%5C%5C%5C%5C%20I_D%20%3D%20%5Cfrac%7BZ%7D%7BL%7D%5Cint_%7B0%7D%5E%7BL%7DQ_n%28x%29%5Cnu%28x%29dx%20%5C%3B%5C%3B%5C%3B%5C%3B%20%285%29)

As for the other FETs, we derive the current equations with different assumptions on the velocity-field relationships.

#### Constant MObility
With constant mobility, the drift velocity and drain current are simply given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cnu%28x%29%20%3D%20%5Cmu%20%5Cxi%28x%29%20%3D%20%5Cmu%20%5Cfrac%7Bd%5CDelta%20%5Cpsi%7D%7Bdx%7D%20%5C%5C%5C%5C%5C%5C%20I_D%20%3D%20%5Cfrac%7BZ%5Cmu%20C_o%7D%7BL%7D%5B%28V_G-V_T%29V_D%20-%20%5Cfrac%7BV_D%5E2%7D%7B2%7D%5D)

In the linear region where VD << ( VG - VT), the above equation is reduced to an ohmic relationship:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_D%20%3D%20%5Cfrac%7BZ%5Cmu%20C_o%28V_G-V_T%29V_D%7D%7BL%7D)

At high VD, Qn(L) at the drain is reduced to zero, corresponding to the pinch-off condition, and current saturates with VD. This gives a saturation drain bias, a saturation drain current and the transconductance of:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20V_D%20%3D%20V_G%20-%20V_T%20%5C%5C%5C%5C%5C%5C%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZ%5Cmu%20C_o%7D%7B2L%7D%20%28V_G-V_T%29%5E2%20%5C%5C%5C%5C%5C%5C%20g_m%20%5Cequiv%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20%5Cfrac%7BZ%5Cmu%20C_o%7D%7BL%7D%20%28V_G-V_T%29)

#### Field-Dependent Mobility
In state-of-the-art devices, current becomes saturated with VD before the pinch-off condition occurs, due to the fact that carrier drift velocity no longer is linearly proportional to the electric field. In other words, in high fields, the mobility becomes field dependent. For devices with high mobilities such as MODFETs, this phenomenon is more severe. The following figure shows the electron velocity-field relationship where a two-piece linear approximation is also shown with a critical field ??<sub>c</sub>. Low-field electron mobilities reported for the AlGaAs/GaAs heterointerface are typically = 1E4 cm2/V.s at 300 K, = 2E5 cm2/V.s at 77 K, and = 2E6 cm2/V.s at 4 K. The mobility enhancement at low temperatures in a MODFET is very pronounced as discussed before. But the improvement of ??s at low temperatures is much less, ranging from 30 to 100%. High mobility also implies low ??<sub>c</sub>, and the drain bias needed to drive the device towards velocity saturation is reduced. From the MOSFET equations, we set M = 1 since the channel doping is very light. Equations of the MOSFET become:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/MODFET_velocity_field.png)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20%5Cfrac%7BZC_o%5Cmu%7D%7BL%7D%28V_G-V_T-%5Cfrac%7BV_%7BDsat%7D%7D%7B2%7D%29V_%7BDsat%7D%20%5C%5C%5C%5C%5C%5C%20V_%7BDsat%7D%20%3D%20L%5Cxi%20_c%20&plus;%20%28V_G-V_T%29%20-%20%5Csqrt%7B%28L%5Cxi%20_c%29%5E2%20&plus;%20%28V_G-V_T%29%5E2%7D)

#### Velocity Saturation
In the case of short-channel devices, complete velocity saturation is approached and simpler equations can be used. The saturation current in this
regime becomes:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_%7BDsat%7D%20%3D%20ZQ_n%5Cnu_s%20%3D%20ZC_o%28V_G-V_T%29%5Cnu_s%20%5C%5C%5C%5C%20g_m%20%5Cequiv%20%5Cfrac%7BdI_%7BDsat%7D%7D%7BdV_G%7D%20%3D%20ZC_o%5Cnu_s)

Notice that in this extreme case IDsat, is independent of L and gm is independent of L and VG.

#### Equivalent Circuit and Microwave Performance
For discussions on small-signal equivalent circuit, f<sub>T</sub>, f<sub>max</sub>, and noise, we can follow the analysis either in MOSFET or MESFET/JFET in the earlier part of this chapter. From the equivalent circuit, in the presence of parasitic source resistance, the extrinsic transconductance g<sub>mx</sub>, the cutoff frequency f<sub>T</sub>, the maximum frequency of oscillation f<sub>max</sub>, and the minimum noise figure F<sub>min</sub> are given exactly with the same equation used for JFET and MESFET.

The speed of MODFETs is higher than that of MESFETs, due to the higher mobilities. Even though the saturation velocities of these devices are comparable, higher mobility pushes the device toward the performance limit of complete velocity saturation. So for the same channel length, higher mobility always gives somewhat higher current and transconductance. Some examples of analog applications are low-noise small-signal amplifiers, power amplifiers, oscillators, and mixers. For digital applications, there are high-speed logic and RAM circuits. MODFET also has superior noise performance compared to other FETs. This improved noise property comes from higher current and transconductance.

Compared to the MESFET, the MODFET can support higher gate bias due to the additional barrier of the AlGaAs layer. It also has better scaling capability since it does not have the restriction associated with the channel depth. Another advantage is lower-voltage operation because of the low ??<sub>c</sub> needed to drive the device into velocity saturation. One drawback of the MODFET is the limit of maximum charge-sheet density at the heterointerface which limits the maximum current drive. 

#### Advanced Device Structures
The major development effort for MODFETs has been on a channel material that can further improve the electron mobility. Instead of GaAs, In<sub>x</sub>Ga<sub>1-x</sub>As has been pursued due to its smaller effective mass. Additional advantages include a larger ??E<sub>C</sub> because of the smaller bandgap. Its higher satellite band has less transfer-electron effect that degrades the mobility. These advantages are found to be directly related to the indium contents: the higher the percentage, the higher the performance.

Introduction of indium in InGaAs causes lattice mismatch to the GaAs substrate. However, growth of good-quality heteroepitaxial layer is still possible provided the epitaxial-layer thickness is under the so-called critical thickness, in which condition the epitaxial layer is under strain. Such technique yields a pseudomorphic InGaAs channel layer and the device is called pseudomorphic MODFET (P-MODFET or P-HEMT). The following figure summarizes the In% range for conventional MODFETs and P-MODFETs, on both GaAs and InP substrates. On GaAs substrate, P-MODFETs can accommodate a maximum of 35% indium. On InP substrate, an unstrained conventional MODFET starts with 53% In, and its P-MODFETs can contain as high as 80% In. So MODFET performance on InP substrate is always higher. The penalty is the higher cost of the InP substrate. In addition, an InP substrate is more susceptible to breakage during processing, and the wafer size is also smaller. These contribute to even higher cost. In general, P-MODFETs are sensitive to changes in strain during processing. Thermal budget has to be minimized to prevent relaxation of the pseudomorphic layer and introduction of dislocations that reduce the carrier mobility. 

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/MODFET_advanced_structure.png)

Yet another approach, depicted in Fig. 23c, is the latest innovation to obtain high In% on GaAs substrate. In this scheme, a thick buffer layer of graded composition is grown on the GaAs substrate. This thick buffer layer serves to transform the lattice constant gradually, from that of the GaAs substrate to whatever required for the subsequent growth of the InGaAs channel layer. In doing so, all the dislocations are contained within the buffer layer. The InGaAs channel layer is unstrained and dislocation-free. Such technique has permitted indium as high as 80%. The resultant MODFET is called metamorphic MODFET (M-MODFET).

Another material system for MODFET that has attracted increased interest recently is based on the AlGaN/GaN heterojunction. GaN has high energy gap (3.4 eV) and is attractive for power applications because of a low ionization coefficient and thus high breakdown voltage. One interesting feature of the AlGaN/GaN system is the additional carriers coming from the effects of spontaneous polarization and piezoelectric polarization, apart from the modulation doping, resulting in higher current capability. In some cases, the AlGaN barrier layer is undoped and excess carrier concentration relies on these polarization effects.

The following figure shows the inverted MODFET structure where the gate is placed over the channel layer rather than the barrier layer which is now grown
over the substrate directly.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/MODFET_Super.png)

In modulation doping, the high-Eg, layer thickness determines the built-in potential ??<sub>P</sub> and preferably cannot be too thin. The channel layer does not have this restriction and can be thinner than the barrier layer. This gives a higher gate capacitance and thus higher transconductance and f<sub>T</sub>. Another advantage is improved source and drain contact resistance since the contacts do not have to go through the high-E, layer. The quantum-well MODFET, sometimes called a double-heterojunction MODFET, is shown in Fig. 24b. Because there are two parallel heterointerfaces, the maximum charge sheet and current are doubled. Another advantage is that the channel is sandwiched by two barriers, and the carriers have better confinement. Multiple-quantum-well structures also have been fabricated based on this principle. In the superlattice MODFET, the superlattice is used as the barrier layer (Fig. 24c). Within the superlattice, the narrow-Eg layers are doped while the wider-Eg layers are undoped. This structure eliminates traps in the AlGaAs layer, and also the parallel conduction path within this doped AlGaAs layer.
