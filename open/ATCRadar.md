# Uncategorized / Unordered questions
- Which different types of radars (in terms of power, accuracy, range, ...) are used and wich type is used for what?
- Most bigger airports have (afaik) their own local weather radars to detect i.e. microbursts. Does ATC also use "large area" weather radar?
- What impact does weather have on properties like range, accuracy, ...
- Redundancy in radar systems?
- Are the ATC radar stations typically connected to each other (in the sense that a controller at airport x can also pull up information from a radar at airport y on her screen)?



Secondary
--------------------------

* History: 
  - IFF
  - How long after primary?
  - When primary?

* How does it work in principle?
  - Sending "something else" actively, not just echo
  - Assumes cooperative targets
  
* Modern Transponder
  - Mode A: squak
  - Mode C: + alt
  - Mode S
  
* Mode A/C
  - is there technical integration (except coloc antennas) with prim?
  - prim radar sends signal 1030 and a/c creates an echo: 
    . direction
    . (diag) range, through time measurement
      (is this done on echo or on active 1090 reply)
  - replies at sep freq: contains data  
    ident based on assigned squawk
  - How is IFF different?
  - "Interrogation" 
    . how encoded?
    . different replies, different interrogations? 
  - (this is all analog tech, right?)
  - Reply: 
    . bandwidth and data encoding?
    . how is data encoded?
    . not self-describing => need to know mode
    . what can be encoded? Is Squawk Ident special?
  - Problem of overlap and garbling. 
    . No Parity Flag.
    . What is done to de-garble?
  
  - PRF and Interlace (17)
  - Precise Bearing (18)
    . Sliding Window Azimuth
    . Monopulse azimuth
  - Plot Extraction (22)
  - Side Lobe Suppression (23)
  
  -> All kinds of limitations... (28)
    -> Mode S
    
* Mode S
  - Core benefits (30)
  - Timeline (30 years!!!!!)
  - 24 bit unique Address - like MAC Address :-) (33f)
  - Interrogation modes: All, Roll, + A/C (34)
    how often which?
  - Interrogation (Message) Structure
    Encoding (Phase Shift)
    Interop with Mode A/C (37)
  - Interrogation formats
  - Replies are Manchester Encoded. Meaning? (40ff)
    different message types encoded at beginning 
  - Actually Sessions/Protocol with several steps
    1) Acquire: identify. No output.
    2) Roll Call Start (no selectivity here!)
    3) Maintain
    4) Lock out (still safe??)
  - What kinds of identifiers and why?
    . Interrogator identifier
    . Surveillance Identifier
  - What is the lockout, and why is it useful?
    Selectivity!
    Area?
  - Active Coordination of multiple radars, data exchange.
  - Error Correction in Mode S - different from earlier modes!
    . Analytic
    . Brute Force
    What is the confidence bitmap?
  - Side Lobe Suppression for Mode S
    How?
    Why different?
  - How is backward compatibility of Mode S transponders to old
    Mode A/C interrogators achieved? 
  - What about general datalink in Mode S?
    Weather, Routing information, ATC clearances 
    Why not really used in practice?
  - Elementary Surveillance 
    Enhanced Surveillance
  - GICB, BDS registers
  - 
  

* Do we still need primary? Or everything ADS-B?  



