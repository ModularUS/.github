# <img src="modularus-logo.svg" width="42" alt="ModularUS mark" align="absmiddle"> ModularUS

**Modular ultrasound systems and algorithms.**<br>
Open hardware, firmware, software, and intelligence for wearable and research ultrasound.

ModularUS grows out of **ModulUS**, the modular design platform for wearable ultrasound we introduced at the IEEE International Ultrasonics Symposium ([Leitner et al., IEEE IUS 2025](https://doi.org/10.1109/IUS62464.2025.11201551)): a sandbox that exposes the pulser, the analog front-end, and the control and compute unit as swappable modules, so that every layer of a wearable ultrasound system can be developed, characterised, and exchanged independently. ModularUS extends that idea from a single platform to an ecosystem, hosting the design platforms, tools, and measurement assets used to architect wearable ultrasound systems before they shrink into a wearable form factor, a role complementary to the wearable device platforms themselves ([Kupsch et al., *Nature Sensors*, 2026](https://doi.org/10.1038/s44460-026-00118-z)).

## Core platform

**ModulUS** ([Leitner et al., IEEE IUS 2025](https://doi.org/10.1109/IUS62464.2025.11201551)) is the reference design platform of the ModularUS ecosystem: a modular four-board sandbox integrating a 32-channel pulser, an analog front-end with bandwidth reduction, and an MCU-based control and compute unit for developing high-resolution wearable ultrasound systems. The open hardware release accompanies the upcoming journal extension.

## State of the art

Two architectural templates dominate wearable ultrasound today: MCU-based systems with few receive channels, and FPGA-based systems with higher channel counts ([Leitner et al., IEEE IUS 2025](https://doi.org/10.1109/IUS62464.2025.11201551)). Normalising the power per receive channel to the excitation frequency makes the architectures comparable across operating points. PuLsE, developed on ModulUS, is the most power-efficient wearable ultrasound system reported to date: 5.8 mW per receive channel, or 0.6 mW/MHz when normalised to the excitation frequency.

| Platform | Topology | Rx channels | Volume [cm³] | Power / Rx [mW] | Excitation f [MHz] | Power / Rx / f [mW/MHz] |
|---|---|---|---|---|---|---|
| WULPUS (Frey et al., IEEE IUS 2022) | MCU | 1 | 14.95 | 22 | 4 | 5.5 |
| USoP (Lin et al., *Nat. Biotechnol.* 2024) | MCU | 1 | 16.2 | 614 | 6 | 102.3 |
| TinyProbe (Vostrikov et al., IEEE T-UFFC 2025) | FPGA | 32 | 39.9 | 30.3 | 15 | 2.0 |
| **PuLsE** ([Giordano et al., IEEE IoT Journal, 2025](https://doi.org/10.1109/JIOT.2025.3581380)) | MCU | 1 | 12.6 | 5.8 | 10 | **0.6** |

Data from Table I of [Leitner et al., IEEE IUS 2025](https://doi.org/10.1109/IUS62464.2025.11201551), which carries the full sources and measurement conditions.

## Repositories

Everything the organisation currently collects. Core repositories are built and maintained here. Forks aggregate results that grew out of our research and remain on the accounts of the students and collaborators who built them, unchanged.

| Repository | Layer | Origin | What it is | Reference |
|---|---|---|---|---|
| [xMasonV2](https://github.com/ModularUS/xMasonV2) | `td` | core | Transfer-matrix simulation framework for multilayer piezoelectric ultrasound transducers | [Spisani et al., IEEE IUS 2025](https://doi.org/10.1109/IUS62464.2025.11201533) · [DOI 10.5281/zenodo.22117703](https://doi.org/10.5281/zenodo.22117703) |
| [croc-4-ultrasound](https://github.com/ModularUS/croc-4-ultrasound) | `el` | fork | IC design: Croc RISC-V SoC with the integrated ultrasound pulser, taped out in IHP 130 nm | [ETH IIS chip gallery, 2026](http://asic.ethz.ch/2026/Pulser.html) |
| [pulser](https://github.com/ModularUS/pulser) | `el` | fork | IC design: BioPULP Pulser, a synthesizable multi-channel ultrasound pulser IP for the Croc RISC-V SoC | IEEE IUS 2026 |
| [UbpS](https://github.com/ModularUS/UbpS) | `fw` | fork | Real-time continuous blood pressure sensing on an ultrasound IoT node, code and data | in review |
| [Ultrasound-Heart-Rate](https://github.com/ModularUS/Ultrasound-Heart-Rate) | `fw` | fork | PuLsE: wrist-worn ultrasound heart-rate monitoring, code, firmware, and data | [Giordano et al., IEEE IoT Journal, 2025](https://doi.org/10.1109/JIOT.2025.3581380) |
| [dasIT](https://github.com/ModularUS/dasIT) | `sw` | core | Delay-and-sum beamformer for plane-wave ultrasound in Python, with a Colab sandbox | — |
| [PEtracer](https://github.com/ModularUS/PEtracer) | `mi` | fork | PEtra: open polarisation-electric-field loop tracer for P(VDF-TrFE) transducer characterisation | [Wessner et al., IEEE UFFC-JS 2024](https://doi.org/10.1109/UFFC-JS60046.2024.10793576) |
| [anatomy-wearable-US-system](https://github.com/ModularUS/anatomy-wearable-US-system) | `edu` | core | Guided Colab exercises on wearable ultrasound system design, built around the ModulUS digital twin: how frequency, channels, pulse rate, and data representation set data rate, power, and battery size | [DOI 10.5281/zenodo.21023566](https://doi.org/10.5281/zenodo.21023566) · [slides DOI 10.5281/zenodo.21030966](https://doi.org/10.5281/zenodo.21030966) |

Layers: `td` transducers · `el` circuits & systems · `fw` firmware · `sw` software · `ml` intelligence · `mi` metrology · `edu` education.

## Ecosystem

Open wearable and research ultrasound projects across the field, at their own homes. Ordered by category, from wearable devices to tools.

| Project | Category | Home | What it is |
|---|---|---|---|
| [WULPUS](https://github.com/pulp-bio/wulpus) | Wearable probe | ETH Zurich (pulp-bio) | Ultra-low-power wearable ultrasound probe |
| [TinyProbe](https://github.com/pulp-bio/TinyProbe) | Wearable probe | ETH Zurich (pulp-bio) | 32-channel multimodal wireless ultrasound probe |
| [un0rick](https://github.com/kelu124/un0rick) | Pulse-echo platform | Luc Jonveaux (kelu124) | Single-board ultrasound hardware (ice40 / Raspberry Pi) |
| [lit3rick](https://github.com/kelu124/lit3rick) | Pulse-echo platform | Luc Jonveaux (kelu124) | up5k pulse-echo acquisition board |
| [pic0rick](https://github.com/kelu124/pic0rick) | Pulse-echo platform | Luc Jonveaux (kelu124) | RP2040-based pulse-echo acquisition platform |
| [Open-LIFU](https://github.com/OpenwaterHealth/openlifu-electrical) | Therapeutic ultrasound | Openwater (OpenwaterHealth) | Open focused-ultrasound platform for neuromodulation, hardware through software |
| [open-UST](https://github.com/morganjroberts/open-UST) | Transducer manufacturing | UCL (morganjroberts) | Manufacturing framework for a 256-element ultrasound tomography ring array |

## About

**Governance.** How repositories are added and maintained: [GOVERNANCE.md](https://github.com/ModularUS/.github/blob/main/GOVERNANCE.md)

**Licensing.** Hardware: Solderpad 2.1. Software and firmware: Apache-2.0. Documentation and data: CC-BY-4.0. Forks keep their upstream licenses.

**Funding.** The core platform work is supported by the Swiss National Science Foundation through the Ambizione project MiNI ([grant 233457](https://data.snf.ch/grants/grant/233457)).

**Contact.** Open an issue in the relevant repository.

## References

- C. Leitner, M. Giordano, M. Tanner, F. Villani, M. Magno, and L. Benini, "ModulUS: A Sandbox for High-Resolution Wearable Ultrasound Development," *IEEE International Ultrasonics Symposium (IUS)*, 2025. [doi:10.1109/IUS62464.2025.11201551](https://doi.org/10.1109/IUS62464.2025.11201551)
- C. Kupsch, C. Leitner, L. Benini, and D. Weik, "Translating wearable ultrasound with system integration and enabling technologies," *Nature Sensors*, 2026. [doi:10.1038/s44460-026-00118-z](https://doi.org/10.1038/s44460-026-00118-z)
- M. Giordano, C. Leitner, C. Vogt, L. Benini, and M. Magno, "PuLsE: Accurate and Robust Ultrasound-Based Continuous Heart-Rate Monitoring on a Wrist-Worn IoT Device," *IEEE Internet of Things Journal*, 2025. [doi:10.1109/JIOT.2025.3581380](https://doi.org/10.1109/JIOT.2025.3581380)
- M.-A. Wessner, F. Villani, S. Papa, K. Keller, L. Ferrari, F. Greco, L. Benini, and C. Leitner, "PEtra: A Flexible and Open-Source PE Loop Tracer for Polymer Thin-Film Transducers," *IEEE Ultrasonics, Ferroelectrics, and Frequency Control Joint Symposium (UFFC-JS)*, 2024. [doi:10.1109/UFFC-JS60046.2024.10793576](https://doi.org/10.1109/UFFC-JS60046.2024.10793576)
- G. Spisani, P. Mayer, S. Papa, F. Greco, M. Magno, L. Benini, and C. Leitner, "xMasonV2: An Open-Source Model Extension for Cascaded Transducer Arrays," *IEEE International Ultrasonics Symposium (IUS)*, 2025. [doi:10.1109/IUS62464.2025.11201533](https://doi.org/10.1109/IUS62464.2025.11201533)
