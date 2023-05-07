# [Superheterodyning](https://en.wikipedia.org/wiki/Superheterodyne_receiver) AM/FM Radio Receiver 

## Finalized Circuit
![image](https://user-images.githubusercontent.com/61887299/236638341-f4ba2f65-112b-481f-ba2a-865e8f8638f5.png)



## Credits
- Dr. Entesari
  - [Tamu Page](https://engineering.tamu.edu/electrical/profiles/kentesari.html)
  - [Google Scholar](https://scholar.google.com/citations?user=_ZYmEFEAAAAJ&hl)
- [ELENCO kit](https://shop.elenco.com/consumers/am-fm-radio-kit-combo-ic-transistor.html)

## Course Description


<p align="center">
![image](https://user-images.githubusercontent.com/61887299/236608637-a8c97562-3681-472e-aec6-9c9105861309.png)
  <img width="460" height="300" src="https://user-images.githubusercontent.com/61887299/236608637-a8c97562-3681-472e-aec6-9c9105861309.png">
</p>

## Project Description
- Soldering, testing dynamically and statically, and verifying superheterodyne AM/FM receiver in conjunction with ECEN-489, Wireless Communications course by Dr. Entesari at Texas A&amp;M, and  the ELENCO AM/FM SUPERHET RADIO kit https://shop.elenco.com/consumers/am-fm-radio-kit-combo-ic-transistor.html 

## Glossary of Terms and Acronyms for common RF design blocks and terms
- <ins>Radio Frequency</ins> **(RF)** - The frequency at which the signal is transmitted through the medium / channel (air)
- <ins>Intermediate Frequency</ins> **(IF)** - The frequency at which teh signal is processed and amplified in the radios electronics ( typically significantly lower than the RF )
- <ins>Local Oscillator</ins> **(LO)** - a radio control block needed to down convert the signal from RF to IF ( interesting trigonemtric identity and problem associated here, but more on that later )
- <ins>Automatic Frequency Control</ins> **(AFC)** - a control feedback methodology for removing variations in the open loop control path from transmitter to receiver for FM receivers
- <ins>Automatic Gain Control</ins> **(AGC)** - a control feedback methodology for removing variations in the open loop control path from transmitter to receiver for AM receivers
- <ins>Low Noise Amplifier</ins> **(LNA)** - a radio design block that is used to amplify the signal strength, the Low noise aspect is important because the amplifier attempts to minimize subsequent distortion in radio design

## Key Takeaways 
- Lab Practicals
  - Soldering approximately 50 total through hole components across AM/FM receiver signal paths, potentiometer volume controller/switch, gang capacitor tuners, and conifugirng/tuning two different antennas for AM/FM respective receivers
- RF Fundamentals
  - Noise Figure
    - Gaussian noise that is non-linear in nature and dominated by the first block of the design. For this reason, in some RF receiver topologies a LNA (Low noise amplifer is used to optimize overall noise figure and SNR, while boosting signal strength at the input)
  - RLC filtering circuit and transformer impedance transformations
    - Q-factor
    - Bandwidth
    - Resonance
    - Maximum Power Transfer
  - Feedback Control
    - For control systems the need to remove uncertainties in the forward path ( antenna to speaker ) is pivotal, the methodology of removing uncertainty is dependent on the way the information is encoded into the analog signal
    - A potential cause of uncertainty is the distance the transmitter is from the receiver and the corresponding energy that the signal will consequently have coming into the antenna
      - To account for this , the kit used a design elemenent known as a varactor, which adjusts for the variations in a feedback loop and creates a robust controlled output
    - Automatic Frequency Control (AFC)
      - For FM the information is in frequency, so an Automatic Frequency Control block must be implemented to remove uncertainties
          - When the frequency was higher the voltage on the varactor would decrease and when the frequency was lower the voltage would increase, which would adapt the local oscillator (LO) operating frequency to keep the IF (Intermediate Frequency) constant
    - Automatic Gain Control (AGC)
      - For AM the information is in frequency, so an Automatic Gain Control(AGC) block must be implemented to remove uncertainties
     
  
## Design Considerations

Discriminator/Detectors ( differentiation to receive FM modulated signal information into amplitude )
- [Foster Seeley](https://en.wikipedia.org/wiki/Foster%E2%80%93Seeley_discriminator) vs. [Ratio Detector](https://en.wikipedia.org/wiki/Ratio_detector)
- [Envelop Detector](https://en.wikipedia.org/wiki/Envelope_detector)


Downconverter ( mixer / oscillation to get sum and difference of RF and LO frequencies to obtain IF frequency )
- Problem of [filtering image frequency](https://en.wikipedia.org/?title=Image_frequency&redirect=no) at output of mixer stage (interference)


[RLC Resonators](https://en.wikipedia.org/wiki/RLC_circuit) ( for channel selection and filtering )
-   High [Q factor](https://en.wikipedia.org/wiki/Q_factor) selectivity to tune channel 


Antennas ( for receiving signal wirelessly )
- AM Antenna utilizes ferrite core and magnetic resonance  
  - AM RF is lower with a longer wavelength so impractical to implement with monopole antenna and must use ferrite core with magentic design
- FM Antenna utilizes monopole topology
  - FM RF is higher with a lower wavelength so practical to implement with monpole antenna for receiving RF signals across air
  
## Regards

I wanted to offer my extended thanks to Dr. Entesari. I know you were doing a lot of work to publish and make advancements in your research: mmWave technology, traveling + family, and recovering from Covid-19 recently. Your help during office hours was invaluable and motivated inspiration for future investigation into challenging work RF engineers are a part of.

![final](https://user-images.githubusercontent.com/61887299/236639110-32417956-10d4-471c-b96b-f9c91d926950.jpg)

  
  
