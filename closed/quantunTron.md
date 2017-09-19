This episode will be about the Quantum Tron: https://www.quantum-systems.com/products/quantum-tron/

------------------------------

* Introduction
  - Florian
  - Background 
  - Ausgründung Uni

* General
  - size, weight, span, payload

* Uses
  - Monitoring of "long" things: pipelines, railtracks
  - Grid'ing, cartography, crop monitoring

  - Talk about typical payloads.

  - Other examples? Military?
    how is operation from ships different? -> landing spot might move :-)
  - Data Link?

  - endurance, range, speeds
  - how much payload is the sweet spot between a/c size and sensor capabilities?
    - what drove the size
    - "Seibel emphasises that complexity, cost and risk rise in a 
       non-linear manner with weight"
      - component complexity and availability
      - heat development and dissipation?

  - Quick assembly
  - Structure: carbon?

* Sensors in the a/c vs. sensors in the payloads.
  - interaction between sensors and a/c: 
    steer around in circle to focus on a place
    (more efficient than hover, I guess)  



* Why VTOL? 
  - Isn't a cat launch plus net landing easier?
  - Complexities added by the VTOL
  - But: simpler wing design - only for high speed


* Propulsion
  - electrical 
  - Zrafeoffs vs. combustion
  - Isn't there waaaay too much power for cruise flight?
  - Switching off two of them for cruise. Good compromise?


    Also the props must be optimized for hover ....
  - Sawtooth for using them at their ideal speed. Gliders :-)
      -> how does this fit with missions?

  - can you land in airplane cfg
  - compensate for 1 engine break
  - Use the rear motors for slowing down. Cool!  

  - Custom developed: 
    - motors
    - controllers
    - propellers
    - power distribution.
    why do so much inhouse?

  - Which batteries? How heavy are the battery packs ? Would it be possible to recharge the batteries on board using solar ?

 


* Control

  - Talk us throught the tilting. Challenges?

  - sensors how much in a/c?    

wind tunnel

  - What is the challenge for the transition? Do you switch between feedback and 
  feedforward controllers? If using feedforward only during the transitions, are 
  there any limits on the disturbances (wind, rain, etc)?

  - diff motor speed vs. nacelle position
    which controls do you use for hovering, controlling a/c there?

  *  what are the wind limits?


  - Which sensors are used as part of the autopilot? What is the "brain" of the Quantum Tron?
  What micro controller? What kind of development: model-based (especially for the controllers)
  or hand-written code, AI? Is it considered safety-critical, standards covered? 

  - What aero surfaces?

prog lang 

* Flying
  - Skills for flying
    One button control -> why? target audience.
  - Remote control vs. autonomous
  
  - Can it fly during nights?
  
  - BVLOS -> what is required, legally? 
  - Sensors for autonomous
    - flying predefined routes with expected free airspace
    - vs. "participarting" in the airspace.
  - Compare to copters?
  - Mission planning and control software
  - Autopilot: IMUs, GNSS -> how accurate?    
    

* Legals/Context
  - where can you use UAVs?
  - which certification must the aircraft obtain ? (EASA, other)
  - airports, max alt?
  - autonomous flying - what preconditions?
  - what are your thoughts (as a glider pilot) of the integration of UAVs/Drones and real airplanes?
    - air spaces
    - alt limitations
    - licensing


* Development
  - How did you get the idea?
  - Which "market studies" led to this configuration?
  - Hardware/Sw in the loop 
  - "enabling it to fly hundreds of simulated Trons at the same time"
  - how many did you crash during development?
    - and why? hardware, ESC turned off, human error?
    - telemetry and data recording. What telemetry system is used under this long range ?
    - This is more serious than model airplanes...
    - human error? -> checklists

* Redundancy 
  - where?
  - what happens if a motor stops during hover?
  - which compromises to make things feasible? IMU voting.


* In terms of components and process, how much does this have in common
  with RC model planes?

encryption

* Who is the dog in the videos?

which wind tunnel?
