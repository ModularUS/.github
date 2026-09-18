# How ModularUS is run

Wearable ultrasound systems today are mainly built as one-off, highly integrated prototypes: change the transducer and you redesign the whole system. ModularUS exists to break that pattern. Our team at ETH Zurich develops ultrasound systems as modules with clear boundaries, from printed piezoelectric transducers, through acquisition electronics and embedded firmware, to processing software and learned signal models, so each layer can be developed, characterised, and exchanged independently ([Leitner et al., IEEE IUS 2025](https://doi.org/10.1109/IUS62464.2025.11201551)).

The pattern serves both ends of development: fast prototyping across the modular stack, and quick integration into specialised devices once a configuration proves itself. PuLsE, the wrist-worn heart-rate monitor developed on ModulUS, runs at 5.8 mW per receive channel, 0.6 mW/MHz normalised to the excitation frequency ([Giordano et al., IEEE IoT Journal, 2025](https://doi.org/10.1109/JIOT.2025.3581380)).

Every platform, tool, and release here is built by the doctoral students, thesis students, and collaborators named in its repository.

## What lives here

- **Core repositories** are built and maintained in this organisation. Each carries a `CITATION.cff` and, on release, a Zenodo DOI, following the [FAIR principles](https://www.go-fair.org/fair-principles/): releases are findable, citable, and licensed for reuse.
- **Linked forks** aggregate results from our projects whose home is the account of the student, collaborator, or partner group that built them. The forks stay untouched: credit, stars, and issues remain with the people who did the work.
- **Ecosystem projects** by other groups are linked from the organisation profile at their own homes, never copied here.

## Layers

Every repository is classified into one of seven layers, shown in the profile tables and as repository topics.

| Layer | Scope |
|---|---|
| Transducers (`td`) | piezoelectric films, acoustic stacks, probes |
| Circuits & systems (`el`) | analog front-ends, pulsers, acquisition electronics, IC to board level |
| Firmware (`fw`) | ultra-low-power acquisition, embedded DSP, drivers |
| Software (`sw`) | beamforming, reconstruction, interfaces, tooling |
| Intelligence (`ml`) | learning on acoustic and multimodal biosignal data |
| Metrology (`mi`) | acoustic and electrical characterisation, test rigs |
| Education (`edu`) | guided design exercises and teaching material |

## How projects are added

A project becomes a core repository when it originates from the team behind ModularUS and someone commits to maintaining it. New projects start here from day one. Repositories keep natural, recognisable names. The layer is assigned as classification, never encoded in the name. Whoever builds them keeps the Maintain role on their repository and is named in the citation file.

## When things appear

Repositories go public when the associated work is published or released. Work in progress is not tracked here.

## Licensing

| Content | License |
|---|---|
| Hardware | Solderpad Hardware License 2.1 |
| Software and firmware | Apache-2.0 |
| Documentation, data, and educational material | CC-BY-4.0 |

Forks keep their upstream licenses.

## Contact

Open an issue in the relevant repository. For everything else, reach out to the [maintainer](https://iis.ee.ethz.ch/people/person-detail.christoph-leitner.html).
