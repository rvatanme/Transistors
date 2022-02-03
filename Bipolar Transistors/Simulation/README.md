# Simulation of a BJT 
The following NPN BJT was simulated using Silvaco.

![](https://github.com/rvatanme/Transistors/blob/main/Bipolar%20Transistors/Simulation/bjt_str.png)

The silvaco input file is as following:

    #TITLE Bipolar Gummel plot and IC/VCE with constant IB
    # Silvaco International 1992, 1993, 1994
    # STRUCTURE SPECIFICATION PART:

    go atlas

    mesh

    x.m l=0 spacing=0.15
    x.m l=0.8 spacing=0.15
    x.m l=1.0 spacing=0.03
    x.m l=1.5 spacing=0.12
    x.m l=2.0 spacing=0.15

    y.m l=0.0 spacing=0.006
    y.m l=0.04 spacing=0.006
    y.m l=0.06 spacing=0.005
    y.m l=0.15 spacing=0.02
    y.m l=0.30 spacing=0.02
    y.m l=1.0 spacing=0.12


    region num=1 silicon


    electrode num=1 name=emitter left length=0.5 y.max=0
    electrode num=2 name=base right length=0.5 y.max=0
    electrode num=3 name=collector bottom


    doping reg=1 uniform n.type conc=5e15
    doping reg=1 gauss n.type conc=1e18 peak=1.0 char=0.2
    doping reg=1 gauss p.type conc=1e18 peak=0.05 junct=0.15
    doping reg=1 gauss n.type conc=5e19 peak=0.0 junct=0.05 x.right=0.8
    doping reg=1 gauss p.type conc=5e19 peak=0.0 char=0.08 x.left=1.5


    # MATERIALS MODELS SPECIFICATION
    # set bipolar models
    models conmob fldmob consrh auger print
    contact name=emitter n.poly surf.rec


    # NUMERICAL SOLUTION PART – SOLUTION SPECIFICATION
    # Initial solution part
    solve init
    save outf=bjtex04_0.str
    tonyplot bjtex04_0.str -set bjtex04_0.set


    # Gummel plot: IB, IC vs. VBE for fixed VCE
    method newton autonr trap
    solve vcollector=0.025
    solve vcollector=0.1
    solve vcollector=0.25 vstep=0.25 vfinal=2 name=collector
    solve vbase=0.025
    solve vbase=0.1
    solve vbase=0.2
    log outf=bjtex04_0.log
    solve vbase=0.3 vstep=0.05 vfinal=1 name=base
    tonyplot bjtex04_0.log -set bjtex04_0_log.set


    #IC vs. VCE with constant IB
    #Ramp Vb
    log off
    solve init
    solve vbase=0.025
    solve vbase=0.05
    solve vbase=0.1 vstep=0.1 vfinal=0.7 name=base


    #Switch to current boundary conditions
    contact name=base current


    #Ramp IB and save solutions
    solve ibase=1.e-6
    save outf=bjtex04_1.str master
    solve ibase=2.e-6
    save outf=bjtex04_2.str master
    solve ibase=3.e-6
    save outf=bjtex04_3.str master
    solve ibase=4.e-6
    save outf=bjtex04_4.str master
    solve ibase=5.e-6
    save outf=bjtex04_5.str master


    #Load in each initial guess file and ramp VCE
    load inf=bjtex04_1.str master
    log outf=bjtex04_1.log
    solve vcollector=0.0 vstep=0.25 vfinal=5.0 name=collector
    load inf=bjtex04_2.str master
    log outf=bjtex04_2.log
    solve vcollector=0.0 vstep=0.25 vfinal=5.0 name=collector
    load inf=bjtex04_3.str master
    log outf=bjtex04_3.log
    solve vcollector=0.0 vstep=0.25 vfinal=5.0 name=collector
    load inf=bjtex04_4.str master
    log outf=bjtex04_4.log
    solve vcollector=0.0 vstep=0.25 vfinal=5.0 name=collector
    load inf=bjtex04_5.str master
    log outf=bjtex04_5.log
    solve vcollector=0.0 vstep=0.25 vfinal=5.0 name=collector



    # RESULTS DISPLAY USING TONYPLOT
    # plot results
    tonyplot -overlay bjtex04_1.log bjtex04_2.log bjtex04_3.log bjtex04_4.log bjtex04_5.log -set
    bjtex04_1_log.set


    # PROGRAM TERMINATION
    quit

Simulating Silicon Bipolar Devices (p 283, atlas manual)

Here, doped regions is defined by Gaussian distribution. The "peak" value specifies the y coordination of the Gaussian peak where expands along a line from x.left to x.right. If the x.left or x.right is not given, they are assumed to be 0 or the device scale in the x direction. The "conc" value specifies the doping concentration in the peak location. The "char" value gives the rate of doping drop from the "conc" in the y (vertical) direction. The lower "char", the faster doping drop rate. The doping drops off laterally can be specified by "RATIO.LATERAL". The lower "RATIO.LATERAL", the faster laterally doping drop rate. If a Gaussian profile is being added to an area that was already defined with the opposite dopant type, you can use the "JUNCTION" parameter to specify the position of the junction depth instead of specifying the standard deviation using the "CHARACTERISTIC" parameter. 

If you specify the PRINT option within the MODELS statement, the details of material parameters and constants and mobility models will be specified at the start of the run-time output. This is a useful way of checking what parameters values and models are being applied in the simulation. We recommend that you always specify MODELS PRINT in input files.

The "conmob" is the concentration dependent model where the software looks up table valid at 300K for Si and GaAs only and uses simple power law temperature dependence. The "fldmob" is the field dependent mobility model and the model is required to to model any type of velocity saturation effect. The "consrh" is the concentration dependent lifetime carrier and is recommended for Si. The "auger" model is the direct transition of three carriers and important at high current densities.

In the "contact" syntax, the "n.poly" would set the workfunction on the contact to that of n type polysilicon. The SURF.REC parameter to enable surface recombination or BARRIER to enable barrier lowering. Calculation of current boundary conditions is activated by the "CURRENT" parameter in the CONTACT
statement. The current boundary conditions are described by the Kirkhoff relation.

The Newton-Richardson Method is a variant of the Newton iteration that calculates a new version of the coefficient matrix only when slowing convergence demonstrates that this is necessary. An automated Newton-Richardson method is available in ATLAS, and improves performance significantly on most problems. To enable the automated Newton-Richardson Method, specify the "AUTONR" parameter of the METHOD statement.

The "NAME" parameter is required from ramping the base voltage and the electrode name is case-sensitive.

The following Gummel plot was obtained while the voltage of the emittor and collector were kept 0V and 2V, respectively and the voltage of the base was sweept from 0.3V to 1V by 0.05V step.   
