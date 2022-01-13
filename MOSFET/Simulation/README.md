# Simulation of MOSFET
Here, we are attending to simulate the following MOSFET with different characteristics. 

![](https://github.com/rvatanme/Transistors/blob/main/MOSFET/Simulation/MOSFET_str.png)

The following silvaco input file was used to simulate the device.

    # (c) Silvaco Inc., 2015

    ############################################################
    #############  Structure Specification  ####################
    ############################################################
    go atlas

    # define fine mesh at surface
    set surf_a=0.0005

    mesh outf=nmos.str
    x.m l=0    spac=0.2
    x.m l=0.75  spac=0.04
    x.m l=1    spac=0.08
    x.m l=1.17  spac=0.01
    x.m l=1.27  spac=0.01
    x.m l=2    spac=0.2
    y.m l=-0.010 spac=0.005
    y.m l=0    spac=$"surf_a"
    y.m l=0.2    spac=0.02
    y.m l=2    spac=0.5

    region num=1 material=Silicon y.min=0
    region num=2 material=Oxide   y.max=0

    electrode name=gate x.min=0.75 length=0.5    
    electrode name=source y.max=0.0 left length=0.4    
    electrode name=drain y.max=0.0 right length=0.4    
    electrode name=substrate bottom

    doping uniform conc=2e17 p.type
    doping uniform conc=1e20 n.type x.max = 0.75 y.min=0 y.max=0.2
    doping uniform conc=1e20 n.type x.min=1.25 y.min=0 y.max=0.2

    save outf=mos2ex14_0.str


    ######################################################################
    ############## Transfer and Output Characteristics  ##################
    ######################################################################

    ############### Mobility Model 1  ####################################
    go atlas

    mesh inf=mos2ex14_0.str

    contact name=gate n.poly

    models cvt srh  print  
 
    method newton gummel carriers=1 electron
    solve init


    solve vdrain=0.1
    save outf=mosfet01_0.str
    tonyplot mosfet01_0.str

    method gummel newton carriers=1 electron
    log outf=mos2ex14_1.log
    solve vgate=0.0 vfinal=3.0 vstep=0.2 name=gate
    extract name="nvt" (xintercept(maxslope(curve(abs(v."gate"),abs(i."drain")))) \
             -abs(ave(v."drain"))/2.0)
    save outf=mos2ex14_1.str

    log outf=IdVd_1.log
    solve vdrain=0 vfinal=3 vstep=0.05 name=drain
    save outf=mosfet_1.str

    quit

In the above example, one can see that there is difference between "electro" and "contact" syntax. In the "electro" syntax, only the location and name of an electrode are specified. But in the "contact" syntax (if there is any), the properties such as workfunction, the material, etc. are determined for a given electrode. 

In the model section, the "cvt" is Lombardi model that include commpletr effect of N (doping concentration), T and both parallel and vertical electric field effects on carrier mobility and is good for non-polar materials. 

The isothermal drift diffusion model requires the solution of three equations for potential, electron concentration, and hole concentration. Specifying GUMMEL or NEWTON alone will produce simple Gummel or Newton solutions. Generally, the GUMMEL method is useful where the system of equations is weakly coupled but has only linear convergence. The NEWTON method is useful when the system of equations is strongly coupled and has quadratic convergence. For almost all cases, the NEWTON method is preferred and it is the default. Specifying:

METHOD GUMMEL NEWTON

will cause the solver to start with GUMMEL iterations. Then, switch to NEWTON if convergence is not achieved. This is a robust but a more time consuming way of obtaining solutions for any device. This method, however, is highly recommended for all simulations with floating regions such as SOI transistors. A floating region is defined as an area of doping, which is separated from all electrodes by a pn junction.

The "extract" syntax extracts the threshold voltage of the MOSFET by calculating the maximum slope of the Id/Vg curve, finding the intercept with the X axis and then subtracting half of the applied drain bias. By default, the extract results is saved in the results.final file. 

The following drain current vs voltage drain for two different gate voltages were obtained from runnening the above silvaco input file.

![]()
