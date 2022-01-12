# Simulation of HEMT

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
