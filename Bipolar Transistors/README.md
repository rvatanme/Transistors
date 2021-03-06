# Bipolar Transistor
The transistor (contraction for transfer resistor) is  a multijunction semiconductor device. Normally, the transistor is  integrated with other circuit 
elements for voltage gain, cur- rent gain, or  signal-power gain. The bipolar transistor, also called the bipolar junction transistor (BJT), is  one of 
the most important semiconductor devices. It has been used extensively in high-speed circuits, analog circuits, and power applications. Bipolar devices 
are semiconductor devices in which both electrons and holes participate in the conduc- tion process. This is in contrast to the field-effect devices.

Thyristor is a closely related bipolar device that will be introduced. The basic thyristor has three closely coupled p-n junctions in the form of 
a p-n-p-n strcture. The device exhibits bistable characteristics and can be switched between a high-impedance "off" state and a low-impedance "on" state.
The name thyristor is derived from gas thyratron, which is a gas-filled tube with similar bistable characteristics. Because of the two stable state 
(on and off) and the low power dissipation in these states, thyristors are useful in many applications.

## General Structure of BT
An idealized, one-dimensional structure of a p-n-p bipolar transistor is shown in the following figure a. Normally, the bipolar transistor has three separately doped regions and two p-n junctions. The heavily doped p<sup>+</sup>-region is called the emitter (defined as symbol E in the figure). The narrow central n-region, with moderately doped concentration, is called the base (symbol B). The width of the base is small compared with the minority-carrier diffusion length. The lightly doped p-region is called the collector (symbol C). The doping concentration in each region is assumed to be uniform. It should be noted that the concepts developed for the p-n junction can be applied directly to the transistor. The figure b illustrates the circuit symbol for a p-n-p transistor. In the active mode, the emitter-base junction is forward biased (V<sub>EB</sub> > 0) and the base-collector junction is reverse biased (V<sub>BC</sub> > 0). According to Kirchhoffs circuit laws, there are only two independent currents for this three-terminal device. If two currents are known, the third current can be obtained. The n-p-n bipolar transistor is the complementary structure of the p-n-p bipolar transistor.

![](https://github.com/rvatanme/Transistors/blob/main/Bipolar%20Transistors/BT_Stru.png)

The following figure a show an idealized p-n-p transistor in thermal equilibrium, that is, where all three leads are connected together or all are grounded. The depletion regions near the two junctions are illustrated by colored areas. Figure b shows the impurity densities in the three doped regions, where the emitter is more heavily doped than the collector. However, the base doping is less than the emitter doping, but greater than the collector doping. Figure c shows the corresponding electric-field profiles in the two depletion regions. Figure d illustrates the energy band diagram, which is a simple extension of the thermal-equilibrium situation for the p-n junction as applied to a pair of closely coupled p<sup>+</sup>-n and n-p junctions. At thermal equilibrium there is no net current flow, hence the Fermi level is a constant in the regions.

![](https://github.com/rvatanme/Transistors/blob/main/Bipolar%20Transistors/pnp-sche.png)

The following figure shows the corresponding cases when the pnp transistor is biased in the active mode. Figure a is a schematic of the transistor connected as an amplifier with the common-base configuration, that is, the base lead is common to the input and output circuits. Figures b and c show the charge densities and the electric fields, respectively, under biasing conditions. Note that the depletion layer width of the emitter-base junction is narrower and the collector-base junction is wider, compared with the equilibrium case.

![](https://github.com/rvatanme/Transistors/blob/main/Bipolar%20Transistors/pnp_bias.png)

Figure d shows the corresponding energy band diagram under the active mode. Since the emitter-base junction is forward biased, holes are injected (or emitted) from the p+ emitter into the base and electrons are injected from the n base into the emitter. Under the ideal-diode condition, there is no generation-recombination current in the depletion region; these two current components constitute the total emitter current. The collector-base junction is reverse biased, and a small reverse saturation current will flow across the junction. However, if the base width is sufficiently narrow, the holes injected from the emitter can diffuse through the base to reach the base-collector depletion edge and then "float up" into the collector (recall the "bubble analogy"). This transport mechanism gives rise to the terminology of emitter, which emits or injects carriers, and of collector, which collects these carriers injected from a nearby junction. If most of the injected holes can reach the collector without recombining with electrons in the base region, then
the collector hole current will be very close to the emitter hole current.

Therefore, carriers injected from a nearby emitter junction can result in a large current flow in a reverse-biased collector junction. This is the transistor action, and it can be realized only when the two junctions are physically close enough to interact in the manner described. Therefore, the two junctions are called the interacting p-n junctions. If, on the other hand, the two junctions are so far apart that all the injected holes are recombined in the base before reaching the base-collector junction, then the transistor action is lost and the p-n-p structure becomes merely two diodes connected back to back.

## Current Gain
The following figure shows the various current components in an ideal p-n-p transistor biased in the active mode. Note that we assume that there are no generation-recombination currents in the depletion regions. The holes injected from the emitter constitute the current I<sub>Ep</sub> which is the largest current component in a well-designed transistor. Most of the injected holes will reach the collector junction and give rise to the current I<sub>Cp</sub>. There are three base current components, labeled I<sub>BB</sub>, I<sub>En</sub>, and I<sub>Cn</sub>. I<sub>BB</sub> corresponds to electrons that must
be supplied by the base to replace electrons recombined with the injected holes (i.e., I<sub>BB</sub> = I<sub>Ep</sub> - I<sub>Cp</sub>). I<sub>En</sub> corresponds to the current arising from electrons being injected from the base to the emitter. However, I<sub>En</sub> is not desirable. It can be minimized by using heavier emitter doping or a heterojunction. I<sub>Cn</sub> corresponds to thermally generated electrons that are near the base-collector junction edge and drift from the collector to the base. As indicated in the figure, the direction of the electron current is opposite the direction of the electron flow.

![](https://github.com/rvatanme/Transistors/blob/main/Bipolar%20Transistors/curr_BT.png)

We can now express the terminal currents in terms of the various current components described above:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_E%20%3D%20I_%7BEp%7D%20&plus;%20I_%7BEn%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20I_C%20%3D%20I_%7BCp%7D%20&plus;%20I_%7BCn%7D%20%5C%5C%5C%5C%20I_B%20%3D%20I_E%20-%20I_C%20%3D%20%28I_%7BEp%7D%20-%20I_%7BCp%7D%29%20&plus;%20%28I_%7BEn%7D%20-%20I_%7BCn%7D%29)

An important parameter in the characterization of bipolar transistors is the common-base current gain ??<sub>0</sub>. This quantity is defined by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Calpha_0%20%5Cequiv%20%5Cfrac%7BI_%7BCp%7D%7D%7BI_E%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%5Calpha_0%20%3D%20%5Cfrac%7BI_%7BCp%7D%7D%7BI_%7BEp%7D&plus;I_%7BEn%7D%7D%20%3D%20%28%5Cfrac%7BI_%7BEp%7D%7D%7BI_%7BEp%7D&plus;I_%7BEn%7D%7D%29%28%5Cfrac%7BI_%7BCp%7D%7D%7BI_%7BEp%7D%7D%29)

The first term on the right-hand side is called the emitter efficiency ??, which is a measure of the injected hole current compared with the total emitter current. The first term on the right-hand side is called the emitter efficiency ??, which is a measure of the injected hole current compared with the total emitter current. Therefore:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cgamma%20%3D%20%5Cfrac%7BI_%7BEp%7D%7D%7BI_E%7D%20%3D%20%5Cfrac%7BI_%7BEp%7D%7D%7BI_%7BEp%7D&plus;I_%7BEn%7D%7D%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5Calpha_T%20%3D%20%5Cfrac%7BI_%7BCp%7D%7D%7BI_%7BEp%7D%7D%20%5C%5C%5C%5C%20%5Calpha_0%20%3D%20%5Cgamma%20%5Calpha%20_T)

For a well-designed transistor, because I<sub>Ep</sub> is small compared with I<sub>Ep</sub> and I<sub>Cp</sub> is close to I<sub>Ep</sub>, both ?? and ??<sub>T</sub>, approach unity. Therefore, ??<sub>0</sub> is close to 1. We can express the collector current in terms of ??<sub>0</sub>. The collector current can be described by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_C%20%3D%20%5Calpha%20_0I_E%20&plus;%20I_%7BCn%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20I_C%20%3D%20%5Calpha%20_0I_E%20&plus;%20I_%7BCBO%7D)

where I<sub>Cn</sub> corresponds to the collector-base current flowing with the emitter open-circuited ( I<sub>E</sub> = 0). We designate I<sub>Cn</sub> as I<sub>CBO</sub>, where the first two subscripts (CB) refer to the two terminals between which the current (or voltage) is measured and the third subscript (O) refers to the state of the third terminal with respect to the second. In the present case, I<sub>CBO</sub> designates the leakage current between the collector and the base with the emitter-base junction open.

## Static Characteristics of BT
In this section, we study the static current-voltage characteristics for an ideal transistor and derive equations for the terminal currents. The current equations are based on the minority-carrier concentration in each region and therefore are described by semiconductor parameters such as doping and minority-carrier lifetime.

To derive the current-voltage expression for an ideal transistor, we assume the following: 1) The device has uniform doping in each region. 2) The hole drift current in the base region as well as the collector saturation current is negligible. 3) There is low-level injection. 4) There are no generation-combination currents in the depletion regions. 5) There are no series resistances in the device. Basically, we assume that holes are injected from the emitter into the base under forward-biased condition. These holes then diffuse across the base region and reach the collector junction. Once we determine the minority-carrier distribution (i.e., holes in the n-type base region), we can obtain the current from the minority-carrier gradient.

The minority-carrier distribution in the neutral base region can be described by the field-free, steady-state continuity equation:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20D_p%28%5Cfrac%7Bd%5E2p_n%7D%7Bdx%5E2%7D%29%20-%20%5Cfrac%7Bp_n%20-%20p_%7Bn0%7D%7D%7B%5Ctau%20_p%7D%20%3D%200)

where D<sub>p</sub>  and ??<sub>p</sub>  are the diffusion constant and the lifetime of minority carriers, respectively. The general solution of the above equation is:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20p_n%28x%29%20%3D%20p_%7Bn0%7D%20&plus;%20C_1e%5E%7Bx/L_p%7D%20&plus;%20C_2e%5E%7B-%5Cfrac%7Bx%7D%7BL_p%7D%7D%20%5C%5C%5C%5C%20p_n%280%29%20%3D%20p_%7Bn0%7Dexp%28%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20p_n%28W%29%20%3D%200)

where Lp = (D<sub>p</sub>??<sub>p</sub>)^0.5 the diffusion length of holes. The constants C, and C, can be determined by the above given boundary conditions for the active mode. The first boundary condition states that under forward bias, the minority-carrier concentration at the edge of the emitter-base depletion region (x = 0) is increased above the equilibrium value by the exponential factor exp(qVEB/kT). The second boundary condition states that under reverse bias, the minority carrier concentration at the edge of the base-collector depletion region (x = W) is zero. By applying the boundary conditions and using the approximation of sinh(W/Lp) = W/Lp where W/Lp close to zero, then the carrier distribution is given by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20p_n%28x%29%20%3D%20p_%7Bn0%7De%5E%7B%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%7D%281-%5Cfrac%7Bx%7D%7BW%7D%29%20%3D%20p_n%280%29%281-%5Cfrac%7Bx%7D%7BW%7D%29)

The distribution approaches a straight line. The approximation is reasonable because the width of the base region is designed to be much smaller than the diffusion length of the minority carrier. The following figure shows a linear minority-carrier distribution in a typical transistor operated under active mode.Note that assuming linear minority-carrier distribution can simplify the derivation of current-voltage characteristics.

![](https://github.com/rvatanme/Transistors/blob/main/Bipolar%20Transistors/Car_dis.png)

The minority-carrier distributions in the emitter and collector can be obtained in a manner similar to the one used to obtain the distributions for the base region. In the above figure, the boundary conditions in the neutral emitter and collector regions are:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20n_E%28x%3D-x_E%29%20%3D%20n_%7BEO%7De%5E%7B%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%7D%20%5C%5C%5C%5C%20n_C%28x%3Dx_C%29%20%3D%20n_%7BCO%7De%5E%7B-q%7CV_%7BCB%7D%7C%7D%3D0)

where n<sub>EO</sub> and n<sub>CO</sub> are the equilibrium electron concentrations in the emitter and collector, respectively. We assume that the emitter depth and the collector depth are much larger than their corresponding diffusion lengths L<sub>E</sub> and L<sub>C</sub>, respectively. Substituting these boundary conditions into expressions similar to:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20n_E%28x%29%20%3D%20n_%7BEO%7D%20&plus;%20n_%7BEO%7D%28e%5E%7B%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%7D-1%29e%5E%7B%5Cfrac%7Bx&plus;x_E%7D%7BL_E%7D%7D%20%5C%5C%5C%5C%20n_C%28x%29%20%3D%20n_%7BCO%7D%20&plus;%20n_%7BCO%7De%5E%7B-%5Cfrac%7Bx-x_C%7D%7BL_C%7D%7D%3D0)

Once the minority-carrier distributions are known, the various current components shown can be calculated. The hole current I<sub>Ep</sub>, injected from the emitter at x = 0, is proportional to the gradient of the minority carrier concentration. For W/Lp << 1, the hole current I<sub>Ep</sub> at x = 0, I<sub>Cp</sub> at x = W, I<sub>En</sub> at -x<sub>E</sub> and I<sub>Cn</sub> at x<sub>C</sub> are first derived and then using those expression, I<sub>E</sub>, I<sub>C</sub> and I<sub>B</sub> are obtained as:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_E%20%3D%20a_%7B11%7D%28e%5E%7B%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%7D-1%29%20&plus;%20a_%7B12%7D%20%5C%5C%5C%5C%20I_C%20%3D%20a_%7B21%7D%28e%5E%7B%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%7D-1%29%20&plus;%20a_%7B22%7D%20%5C%5C%5C%5C%20I_B%20%3D%20%28a_%7B11%7D-a_%7B21%7D%29%28e%5E%7B%5Cfrac%7BqV_%7BEB%7D%7D%7BkT%7D%7D-1%29%20&plus;%20%28a_%7B12%7D-a_%7B22%7D%29)

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20a_%7B11%7D%20%5Cequiv%20qA%28%5Cfrac%7BD_pp_%7Bn0%7D%7D%7BW%7D%20&plus;%20%5Cfrac%7BD_En_%7BEO%7D%7D%7BL_E%7D%29%20%5C%3B%5C%3B%5C%3B%5C%3Ba_%7B12%7D%20%5Cequiv%20%5Cfrac%7BqAD_pp_%7Bn0%7D%7D%7BW%7D%20%5C%5C%5C%5C%5C%5C%20a_%7B21%7D%20%5Cequiv%20%5Cfrac%7BqAD_pp_%7Bn0%7D%7D%7BW%7D%20%5C%3B%5C%3B%5C%3B%5C%3Ba_%7B22%7D%20%5Cequiv%20qA%28%5Cfrac%7BD_pp_%7Bn0%7D%7D%7BW%7D%20&plus;%20%5Cfrac%7BD_Cn_%7BCO%7D%7D%7BL_C%7D%29)

where D<sub>E</sub> and D<sub>C</sub> are the diffusion constants in the emitter and collector, respectively. From these discussions, we see that the currents in the three terminals of a transistor are mainly determined by the minority carrier distribution in the base region. Once we derive the current components, the common-base current gain ??<sub>0</sub>, can be obtained.
