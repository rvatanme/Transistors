# Simulation of HEMT/MESFET/JFET

Here, the following HEMT device is simulated using Silvaco software.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Simulation/hemt_str.png)

The input silvaco file is as following:

    # (c) Silvaco Inc., 2017
    go atlas 

    # Sweep increment
    set vstart = 0
    set vstop = 15
    set vinc = .5

    mesh width=100

    # x plane meshing
    x.m l=0.0 s=0.25
    x.m l=0.5 s=0.25
    x.m l=1.0 s=0.25
    x.m l=3.5 s=0.15
    x.m l=5.5 s=0.15
    x.m l=8 s=0.15
    x.m l=8.5 s=0.25
    x.m l=9 s=0.25

    # y plane meshing
    y.m l=0 s=0.25
    y.m l=0.5 s=0.001
    y.m l=0.525 s=0.001
    y.m l=0.6 s=0.05
    y.m l=0.7 s=0.1
    y.m l=1.0 s=0.2
    y.m l=2.0 s=1

    region num=1 x.min=0 x.max=9 y.min=0.5 y.max=0.525 mat=AlGaN x.comp=0.3 
    region num=2 x.min=0 x.max=9 y.min=0.0 y.max=0.5 mat=nitride insulator
    region num=3 x.min=0 x.max=9 y.min=0.525 y.max=2 mat=GaN substrate 

    elec num=1 name=source x.min=0 x.max=0.5 y.min=0.5 y.max=0.6
    elec num=2 name=drain x.min=8.5 x.max=9 y.min=0.5 y.max=0.6
    elec num=3 name=gate x.min=3.5 x.max=5.5 y.min=0 y.max=0.5 
    elec num=4 substrate

    contact name=gate work=5
    contact name=source work=3.93
    contact name=drain work=3.93

    models print srh 
    mobility albrct.n 
    model polarization calc.strain polar.scale=0.8 

    output con.band val.band charge polar.charge band.par

    method newton trap maxtrap=20

    solve init
    save outf=ganfetex03_0.str

    solve vdrain=1.0
    save outf=hemt01_0.str
    tonyplot hemt01_0.str

    solve name=gate vfinal=-10 vstep=-0.5
    log outf=ganfetex03_0.log
    solve name=gate vfinal=1.0 vstep=0.5
    log off

    solve init
    solve vgate=-3
    log outf=ganfetex03_1.log
    solve name=drain vdrain=$vstart vfinal=$vstop vstep=$vinc
    log off
    #
    solve init
    solve vgate=-2
    log outf=ganfetex03_2.log
    solve name=drain vdrain=$vstart vfinal=$vstop vstep=$vinc
    log off
    #
    solve init
    solve vgate=-1
    log outf=ganfetex03_3.log
    solve name=drain vdrain=$vstart vfinal=$vstop vstep=$vinc
    log off
    #
    solve init
    solve vgate=0
    log outf=ganfetex03_4.log
    solve name=drain vdrain=$vstart vfinal=$vstop vstep=$vinc
    log off

    quit

Polarization in wurtzite materials is characterized by two components, spontaneous polarization Psp and piezoelectric polarization. Therefore, the total polarization is the sum of the both polarization. The Psp is specified on the MATERIAL statement and specifies the total spontaneous polarization.  

To enable the polarization model, specify POLARIZATION in the REGION statement for the region for which you wish to characterize polarization effects. Typically, this will be a quantum well layer or active layer.

The polarization enters into the simulation as a positive and negative fixed charges appearing at the top (most negative Y coordinate) and bottom (most positive Y coordinate) of the layer in question. By default, the positive charge is added at the bottom and the negative charge is added at the top. You can modify the sign and magnitude of this charge by specifying POLAR.SCALE in the REGION statement. This parameter is multiplied by the polarization determined by Equation 3-506 to obtain the applied charge. The default value for POLAR.SCALE is 1.0.

If you want to also include piezoelectric polarization, you can also specify the CALC.STRAIN parameter. If you specify CALC.STRAIN, the simulator will
automatically calculate strain from the lattice mismatch and will calculate the piezoelectric polarization and apply it to the region. You can also specify the value of the STRAIN parameter, which specifies the axial strain in the region. With STRAIN and POLARIZATION set, the simulator will apply a piezoelectric polarization calculated using the strain value assigned by the STRAIN parameter.

The albrct.n enable the Albrecht mobility model (see Chapter 5: “Blaze: Compound Material 2D Simulator”, “The Albrecht Model” Section on page 5-38).

For MESFET simulation, the following silvaco input file was used:

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Simulation/MESFET_str.png)


    # (c) Silvaco Inc., 2021
    go atlas
    title GaAs MESFET Simulation with EB and DD models
    #
    # SECTION 1: Mesh spectification
    #
    # Define the mesh
    #
    mesh  space.mult=2.0
    # 
    x.mesh loc=0.00 spac=0.02
    x.mesh loc=0.2 spac=0.01
    x.mesh loc=0.4 spac=0.01
    x.mesh loc=0.6 spac=0.02
    #
    y.mesh loc=0.00 spac=0.005
    y.mesh loc=0.2 spac=0.02
    y.mesh loc=1 spac=0.1
    #
    # SECTION 2: Structure and models spectifications
    #
    region     num=1  material=GaAs
    #
    elec       num=1  name=source x.min=0.0 y.min=0.0 x.max=0.1 y.max=0.
    elec       num=2  name=drain  x.min=0.5 y.min=0.0 x.max=0.6 y.max=0. 
    elec       num=3  name=gate   x.min=0.2 length=0.2
    #
    doping uniform conc=1.e15 p.type
    doping uniform conc=1.e17 n.type y.min=0 y.max=0.12
    doping uniform conc=5.e18  n.type x.left=0.  x.right=0.1 y.min=0 y.max=0.05
    doping uniform conc=5.e18  n.type x.left=0.5 x.right=0.6 y.min=0 y.max=0.05
    #
    contact num=3 work=4.87
    #
    ######################################
    #            DD calculation          #
    ######################################
    #
    contact num=3 work=4.87
    models   print  conmob fldmob evsatmod=1  
    material taurel.el=1.e-12 taumob.el=1.e-12 vsat=1.e7
    #
    # SECTION 3: Initial solution
    #
    solve init
    save outf=mesfetex03.str
    #
    tonyplot  mesfetex03.str -set mesfetex03_0.set
    #
    # SECTION 4: Id-Vd characteristics
    # 
    method newton  maxtrap=6
    #
    output e.velocity
    #
    probe n.mob max dir=0  name="mux"
    probe n.mob max dir=90 name="muy"
    log outf=mesfetex03_1.log 
    #
    solve vdrain=0.0 vstep=0.05 vfinal=0.5  name=drain 
    method newton
    solve  vdrain=0.6 vstep=0.1 vfinal=2 name=drain 
    save outf=mesfetex03_1.str

    solve vgate=0.2
    log outf=mesfetex03_2.log
    solve vdrain=0.0 vstep=0.05 vfinal=0.5  name=drain 
    method newton
    solve  vdrain=0.6 vstep=0.1 vfinal=2 name=drain 
    save outf=mesfetex03_2.str
    #
    tonyplot  mesfetex03_1.log -overlay mesfetex03_2.log  -set mesfetex03_log.set
    #
    quit

Setting EVSATMOD=1 implements the GaAs carrier temperature dependent mobility model. VSATN and VSATP are the saturation velocities for electrons and holes, and TAUSN and TAUSP correspond to the electron energy relaxation times (TAUREL.EL and TAUREL.HO). The TAUMOB.EL and TAUMOB.HO parameters can be set on the energy balance MODELS statement and have the default values. The Energy Balance Transport Model allows the carrier mobility to be related to the carrier energy. This has been achieved through the homogeneous steady state energy balance relationship that pertains in the saturated velocity limit.  VSAT is the saturation velocities. 

OUTPUT allows you to specify the data that will be stored in standard structure format files. The e.velocity Specifies that the total electron velocity will be included in the standard structure file.

PROBE allows you to output the value of several distributed quantities to the log file. The value at a specified location or the minimum, maximum, or integrated value within a specified area of the device will be saved to the log file at each bias or time point. PROBE is the most accurate way to determine the value of many parameters calculated by ATLAS. Parameters stored on node points in the structure files for TonyPlot are often interpolated and subject to noise. The n.mob specifies that the probe will operate on the electron mobility. The DIR [direction x(0),y(90),z] parameter should also be specified if N.MOB is used.

The following IV curve for mesfet is obtained form running the mentioned silvaco input file.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Simulation/mesfet_IV.png)

The following JFET is simulated using below Silvaco input.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Simulation/JFET_str.png)


    # (c) Silvaco Inc., 2021
    go atlas
    #
    # SECTION 1: Mesh spectification
    #
    # Define the mesh
    #
    mesh  space.mult=2.0
    # 
    x.mesh loc=0.00 spac=0.02
    x.mesh loc=0.4 spac=0.01
    x.mesh loc=0.8 spac=0.01
    x.mesh loc=1.2 spac=0.02
    #
    y.mesh loc=0.00 spac=0.005
    y.mesh loc=0.2 spac=0.02
    y.mesh loc=2 spac=0.1
    #
    # SECTION 2: Structure and models spectifications
    #
    region     num=1  material=Si
    #
    elec       num=1  name=source x.min=0.0 y.min=0.0 x.max=0.1 y.max=0.
    elec       num=2  name=drain  x.min=1.1 y.min=0.0 x.max=1.2 y.max=0. 
    elec       num=3  name=gate   x.min=0.5 length=0.2
    #
    doping uniform conc=1.e15 p.type
    doping uniform conc=1.e16 n.type y.min=0 y.max=1.0
    doping uniform conc=1.e20 p.type x.min=0.5 x.max=0.7 y.min=0 y.max=0.05
    doping uniform conc=5.e18  n.type x.left=0.  x.right=0.1 y.min=0 y.max=0.05
    doping uniform conc=5.e18  n.type x.left=1.1 x.right=1.2 y.min=0 y.max=0.05
    #
    #
    ######################################
    #            DD calculation          #
    ######################################
    #

    models cvt srh  print  
 
    method newton gummel carriers=1 electron
    solve init

    solve vgate=-0.5
    save outf=jfet01_0.str
    tonyplot jfet01_0.str

    solve vgate=0.0
    save outf=jfet01_1.str
    #tonyplot jfet01_1.str

    solve vgate=0.5
    save outf=jfet01_2.str
    #tonyplot jfet01_2.str

    solve vgate=-0.5
    method gummel newton carriers=1 electron
    log outf=jfet01_1.log
    solve vdrain=0 vfinal=3 vstep=0.05 name=drain

    solve vgate=0.5
    method gummel newton carriers=1 electron
   log outf=jfet01_2.log
   solve vdrain=0 vfinal=3 vstep=0.05 name=drain

    #
    tonyplot  jfet01_1.log -overlay jfet01_2.log
    #
    quit
   
The following IV curve for JFET was obtained from running above the input file.

![](https://github.com/rvatanme/Transistors/blob/main/JFET_MESFET_MODFET/Simulation/IV_JFET.png)
