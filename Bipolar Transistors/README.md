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

An important parameter in the characterization of bipolar transistors is the common-base current gain α<sub>0</sub>. This quantity is defined by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Calpha_0%20%5Cequiv%20%5Cfrac%7BI_%7BCp%7D%7D%7BI_E%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20%5Calpha_0%20%3D%20%5Cfrac%7BI_%7BCp%7D%7D%7BI_%7BEp%7D&plus;I_%7BEn%7D%7D%20%3D%20%28%5Cfrac%7BI_%7BEp%7D%7D%7BI_%7BEp%7D&plus;I_%7BEn%7D%7D%29%28%5Cfrac%7BI_%7BCp%7D%7D%7BI_%7BEp%7D%7D%29)

The first term on the right-hand side is called the emitter efficiency γ, which is a measure of the injected hole current compared with the total emitter current. The first term on the right-hand side is called the emitter efficiency γ, which is a measure of the injected hole current compared with the total emitter current. Therefore:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20%5Cgamma%20%3D%20%5Cfrac%7BI_%7BEp%7D%7D%7BI_E%7D%20%3D%20%5Cfrac%7BI_%7BEp%7D%7D%7BI_%7BEp%7D&plus;I_%7BEn%7D%7D%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5Calpha_T%20%3D%20%5Cfrac%7BI_%7BCp%7D%7D%7BI_%7BEp%7D%7D%20%5C%5C%5C%5C%20%5Calpha_0%20%3D%20%5Cgamma%20%5Calpha%20_T)

For a well-designed transistor, because I<sub>Ep</sub> is small compared with I<sub>Ep</sub> and I<sub>Cp</sub> is close to I<sub>Ep</sub>, both γ and α<sub>T</sub>, approach unity. Therefore, α<sub>0</sub> is close to 1. We can express the collector current in terms of α<sub>0</sub>. The collector current can be described by:

![](https://latex.codecogs.com/svg.latex?%5CLARGE%20I_C%20%3D%20%5Calpha%20_0I_E%20&plus;%20I_%7BCn%7D%20%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%5C%3B%20I_C%20%3D%20%5Calpha%20_0I_E%20&plus;%20I_%7BCBO%7D)

where I<sub>Cn</sub> corresponds to the collector-base current flowing with the emitter open-circuited ( I<sub>E</sub> = 0). We designate I<sub>Cn</sub> as I<sub>CBO</sub>, where the first two subscripts (CB) refer to the two terminals between which the current (or voltage) is measured and the third subscript (O) refers to the state of the third terminal with respect to the second. In the present case, I<sub>CBO</sub> designates the leakage current between the collector and the base with the emitter-base junction open.
