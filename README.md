# [Superheterodyning](https://en.wikipedia.org/wiki/Superheterodyne_receiver) AM/FM Radio Receiever 

## Credits
- Dr. Entesari
  - [Tamu Page](https://engineering.tamu.edu/electrical/profiles/kentesari.html)
  - [Google Scholar](https://scholar.google.com/citations?user=_ZYmEFEAAAAJ&hl)
- [ELENCO kit](https://shop.elenco.com/consumers/am-fm-radio-kit-combo-ic-transistor.html)

## Course Description

![image](https://user-images.githubusercontent.com/61887299/236608637-a8c97562-3681-472e-aec6-9c9105861309.png)


## Project Description
- Soldering, testing dynamically and statically, and verifying superheterodyne AM/FM receiver in conjunction with ECEN-489, Wireless Communications course by Dr. Entesari at Texas A&amp;M, and  the ELENCO AM/FM SUPERHET RADIO kit https://shop.elenco.com/consumers/am-fm-radio-kit-combo-ic-transistor.html 

## Key Takeaways 
- Lab Practicals
  - Soldering approximately 50 total through hole components across AM/FM receiver signal paths, potentiometer volume controller/switch, gang capacitor tuners, and conifugirng/tuning two different antennas for AM/FM respective receivers
- RF Fundamentals
  - Noise Figure
    - Gaussian noise that is non-linear in nature and dominated by the first block of the design. For this reason, in some RF receiver topologies a LNA (Low noise amplifer is used to optimize overall noise figure and SNR, while boosting signal strength at the input)
  - RLC filtering circuit and transformer impedance transformations
    - Q-factor
    - Bandwidth
  
## Design Considerations

Discriminator ( differentiation to receive FM modulated signal information into amplitude )
- [Foster Seeley](https://en.wikipedia.org/wiki/Foster%E2%80%93Seeley_discriminator) vs. [Ratio Detector](https://en.wikipedia.org/wiki/Ratio_detector)


Downconverter ( mixer / oscillation to get sum and difference of RF and LO frequencies to obtain IF frequency )
- Problem of [filtering image frequency](https://en.wikipedia.org/?title=Image_frequency&redirect=no) at output of mixer stage (interference)


[RLC Resonators](https://en.wikipedia.org/wiki/RLC_circuit) ( for channel selection and filtering )
-   High [Q factor](https://en.wikipedia.org/wiki/Q_factor) selectivity to tune channel 


Antennas ( for receiving signal wirelessly )
- AM Antenna utilizes ferrite core and magnetic resonance  
  - AM RF is lower with a longer wavelength so impractical to implement with monopole antenna and must use ferrite core with magentic design
- FM Antenna utilizes monopole topology
  - FM RF is higher with a lower wavelength so practical to implement with monpole antenna for receiving RF signals across air
  
  
