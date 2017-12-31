Superconductivity
------------------------------------------------

General one on superconductivity and the “usual” LTS materials NbTi and Nb3Sn:
* https://en.wikipedia.org/wiki/Superconductivity
* https://en.wikipedia.org/wiki/Niobium-titanium
* https://en.wikipedia.org/wiki/Niobium-tin


* What is normal conductivity?
  - zero resistance (not just very low)
  - "jump" in conductivity
    . not a continuous reduction.
    . at T = TCrit
* What is superconductivity physically?
  - quantum mech phenomenon
  - Cooper Pairs
  - often R or I is connected to H, what happens to magnetic field?
    - magnetic field ("expelled")
  - Meissner Effect
  - Ginzburg Landau parameter?
  - What is quenching? When/why does it happen?
* Why only at low temperatures?
* Which materials? 
  (for each of them discuss their properties/trade-offs, roughly)
  (this is an overview, we can discuss their use in cables, magnets
  and cavitities when we discuss these applications/componets below)
  - LTS
    . Nb - soft type II
    . NbTi – hard type II
    . Nb3Sn – hard type II
   - HTS
     . Discovery and crystal structure - different mechanism?
     . Superconducting properties – grain boundaries/anisotropy
     . BiSCCO and MgB2 – wires
     . tapes and cable designs
* Different kinds:
  - reponse to magnetic field (and maximum current density)
  - T-crit
  - theory of operation
  - material
* How do we find out about it?
  - history... first discovery?
    Kammerling Onnes 1905 – resistivity of Pb / liquefaction of He and Dewars
  - theoretical models?
  - experiments?
  - serendipidy?
* What are the characteristics we want to get for new SCs
  - higher TCrit (makes cooling easier)
    what are useful "thresholds"?
  - what else?
* Ceramic High Temp superconductors
  - YBCO (with some missing oxygen atoms in the lattice!)
    - Oxides are usually insulators at RT, in contrast to the "classical" superconductors?
  - Perovskites are also hot in Photovoltaics. Any connection there?

Applications
---------------------------------------------------
* Why is superconductors relevant?
  - wouldn't *very low* resistance be good enough?

* Overview End User Applications
  - Early applications – magnets for MRI, maglev
  - High field magnets for science research – accelerators, fusion
  - Grid components – transmission lines, FCLs
  - Superconducting electronics, sensors

Components:
---------------------------------------------------
For all of the applications: discuss their use in ITER and accelerators.
We can/should spend most of our time on the use in magnets, the other
applications we can keep shorter.


* Superconducting wires
    https://en.wikipedia.org/wiki/Superconducting_wire
    http://lss.fnal.gov/archive/2012/conf/fermilab-conf-12-571-td.pdf
  - why? thinner, less heat, ultimately better efficiency ratio
  - Challenges?
    . how do you cool it?
    . avoid quenching, how?
    . How much energy/Helium is needed for cooling and does this limit further application?
    . How do you control the required amount of helium? 
      What does it depend on?
  - Manufacturing
    . What limits the design of magnets (not the material but shapes etc.)? 
      Physical or manufacturing? 
      material properties, brittleness
    . How does one make sure to cool everything? 
      Just place some wires into a bath of liquid Helium 
      or sophisticated cooling techniques?
  - use in ITER?
  - How do you to electrically connect superconducting cold parts with normal 
    temperature conductors. This gets specially interesting with superconductors 
    cooled by liquid helium and high currents in Kiloampere range.
  - The SC is basically a "short circuit" - 
    how do you design a "power supply" for that?
  

* Superconducting Cables:
    https://en.wikipedia.org/wiki/Rutherford_cable
    https://www.cryogenicsociety.org/resources/defining_cryogenics/cable-in-conduit_conductors/
  - sounds like "thicker wires". Difference? 
    multiple wires in one bigger cable
  - plus a coolant - how is it integrated?
    . coolant => free space => movement => heat. How do you solve that?
  - Parameters determining whether a superconducting cable is more economic than suffering the electric losses?
     - AC vs DC?

* Superconducting junctions:
   https://en.wikipedia.org/wiki/Pi_Josephson_junction
   https://en.wikipedia.org/wiki/Josephson_effect
   
* SQUIDs:
    https://en.wikipedia.org/wiki/SQUID
    
* Superconducting RF cavities:
    https://en.wikipedia.org/wiki/Superconducting_radio_frequency
  - what are RF cavities?
  - these are not just wound up wires, how do they work?
    
* Superconducting Magnets:
    https://en.wikipedia.org/wiki/Superconducting_magnet
    http://www.fusionforenergy.europa.eu/mediacorner/newsview.aspx?content=995
    http://lhc-machine-outreach.web.cern.ch/lhc-machine-outreach/components/magnets.htm
  - these are "just" wound up wires - what is the challenge?
  - Accurate field strength, homogeneous fields, field gradients (MRI/NMR machines)
  - Goal is to create strong magnetic field. What limits that? Strongest existing magnets are not superconducting.
    - Heat?
    - Liquid cooling vs. mechanical cooling.
    - Effect of the generated magnetic field on the superconductivity
  - Quenching 
    . the "accident" at LHC
    . how do you design against it?
    . monitoring, detection .. and then?
  - How are supercon magnets protected from heating due to neutrons produced 
    by fusion reactions? Do they all just have very low scattering cross section 
    with the liquid helium coolant and supercon magnet?
  - Other design issues
    . Mechanical
    . Brittleness
    . AC loss – hysteresis and coupling losses in pulsed, fast ramped magnets
    . Explanation of CISCCs, strands, void fraction, fatigue performance
    . QA for the magnets, different production locations, learning curve
  - Repeat the basics of a Tokamak; and how are these SC magnets used here?
    . Copper coils, field lines, maximum current due to resistance and heat
    . How do magnets confine the plasma, ionization, plasma pressure, beta, Lawson criterion, plasma instabilities
    . The end of conventional magnets for fusion
  
 
