# AM Radio Receiver

A tunable AM radio receiver built using analog electronics principles including LC resonance, envelope detection, and audio amplification.

<div align="center">
  <img src="media/radio_pic.jpg" width="500"/>
</div>

---

## Overview

This project implements a functional AM (Amplitude Modulation) radio receiver capable of tuning and demodulating commercial AM broadcast signals.

The radio uses:

* A ferrite rod antenna and LC resonant tank for frequency selection
* A germanium diode envelope detector for AM demodulation
* An LM386 audio amplifier to drive an 8-ohm speaker
* A variable capacitor for manual station tuning

## Features

* Tunable AM broadcast reception
* Ferrite rod antenna front-end
* Analog envelope detection
* Adjustable tuning capacitor
* Audio amplification using LM386
* Fully discrete analog signal chain

---

## How it Works

The ferrite rod antenna coil and variable capacitor form a parallel LC resonant circuit:


$$
f = \frac{1}{2\pi\sqrt{LC}}
$$


By adjusting the capacitance, the resonant frequency changes, allowing the receiver to tune to different AM radio stations.

AM radio stations transmit a high-frequency carrier whose amplitude varies according to the audio signal.

A germanium diode rectifies the RF waveform, while an RC filter extracts the audio envelope.

The recovered audio signal is amplified using an LM386 audio amplifier IC to drive an 8-ohm speaker.

Here is the KiCAD schematic (also available for download in this repository): 

<div align="center">
  <img src="media/radio_schem.jpg" width="500"/>
</div>

---

## Hardware

### Main Components

| Component               | Description                                   |
| ----------------------- | --------------------------------------------- |
| Ferrite Rod Antenna     | RF signal pickup and inductive tuning element |
| Variable Capacitor      | Frequency tuning                              |
| 1N34A Germanium Diode   | Envelope detector                             |
| LM386                   | Audio power amplifier                         |
| 8Ω Speaker              | Audio output                                  |
| Electrolytic Capacitors | Coupling and power filtering                  |
| Ceramic Capacitors      | RF filtering and tuning                       |

---

## Schematic

### KiCad Schematic

The full schematic is available in:

```text
hardware/schematic/
```

Preview:

<div align="center">
  <img src="hardware/schematic/schematic_preview.png" width="700"/>
</div>

---

## Build Process

### Prototype Phase

* Initial RF front-end tested on breadboard
* Audio amplifier validated independently
* RF grounding and resonant behavior debugged iteratively

### Final Assembly

* Circuit assembled on protoboard
* Ferrite antenna integrated into resonant tank
* Manual tuning calibrated across AM band

---

## Key Engineering Challenges

* Achieving stable LC resonance in the AM broadcast band
* Preventing RF tank loading
* Managing grounding and parasitic coupling
* Debugging analog signal paths without oscilloscope access
* Proper antenna and detector coupling

---

## Skills Demonstrated

* Analog circuit design
* RF fundamentals
* Resonant circuit analysis
* Signal demodulation
* Audio amplifier integration
* Schematic capture in KiCad
* Hardware debugging and prototyping

---

## Future Improvements

* Custom PCB design
* Automatic gain control (AGC)
* Regenerative receiver architecture
* Digital frequency display
* Improved selectivity and filtering

---

## Media

### Demonstration Video

(Add project demo video here)

### Audio Reception Samples

(Add recordings of received stations)

---

## Repository Contents

| Folder        | Purpose                            |
| ------------- | ---------------------------------- |
| `docs/`       | Documentation and images           |
| `hardware/`   | KiCad schematic and hardware files |
| `simulation/` | LTspice or MATLAB analysis         |
| `media/`      | Videos and audio demonstrations    |

---

## Author

Benjamin H. Goldstein
