\## Repository Structure



```text

Oben-Contracts/

├─ README.md                      # Overview, vision, quickstart

├─ LICENSE                        # To be added (e.g. MIT or custom)

├─ data/

│  ├─ nodes/

│  │  ├─ OBEN\\\_Master\\\_NodeMap\\\_v2.csv            # Final node + AWS mapping

│  │  ├─ mhd\\\_crypto\\\_nodes\\\_geo\\\_enriched.csv     # Detailed node geodata (from analysis)

│  ├─ edges/

│  │  ├─ mhd\\\_crypto\\\_edges\\\_geo\\\_enriched.csv     # Node-to-node edges + chain links

│  ├─ chains/

│  │  ├─ OBEN\\\_Libra\\\_ChainFlow\\\_v2.csv           # Libra chain hop sequence

│  │  ├─ OBEN\\\_Lithium\\\_ChainFlow\\\_v2.csv         # Lithium chain hop sequence

│  │  ├─ OBEN\\\_Orion\\\_ChainFlow\\\_v2.csv           # Orion chain hop sequence

│  │  ├─ OBEN\\\_Master\\\_ChainFlows\\\_v2.csv         # All three chains merged

│  ├─ tokenomics/

│  │  ├─ Pools\\\_Version\\\_2\\\_base.pdf              # Early pool design reference

│  │  ├─ OBEN\\\_Crypto\\\_Data\\\_Sheet\\\_v1.docx        # Final token + pool parameters

│  └─ misc/

│     ├─ mhd\\\_crypto\\\_edges.csv                   # Older/raw edge data

│     ├─ mhd\\\_crypto\\\_nodes.csv                   # Older/raw node data

│     ├─ unidirectional\\\_loop\\\_with\\\_radials\\\_good\\\_bad.pdf  # Loop topology notes

├─ docs/

│  ├─ whitepaper/

│  │  ├─ OBEN\\\_Whitepaper\\\_v1.docx               # Main protocol whitepaper

│  ├─ architecture/

│  │  ├─ OBEN\\\_4\\\_Layer\\\_Lattice\\\_Summary.pdf      # L0–L3 lattice + layers

│  │  ├─ alpha\\\_omega\\\_mhd\\\_crypto\\\_node\\\_map\\\_geo\\\_enriched.pdf # Annotated geo node map

│  │  ├─ alpha\\\_omega\\\_mhd\\\_crypto\\\_node\\\_map.pdf   # Earlier node-map reference

│  │  ├─ OBEN\\\_Node\\\_Lattice\\\_AlphaOmega\\\_v2.docx  # Conceptual node-lattice spec

│  │  ├─ OBEN\\\_Node\\\_Map\\\_By\\\_Sector\\\_Checklist.docx# Per-sector AWS checklist

│  │  ├─ OBEN\\\_AWS\\\_Build\\\_Sheet\\\_v1.docx          # EC2 build + tagging guide

│  ├─ runbooks/

│  │  ├─ OBEN\\\_Token\\\_Creation\\\_Runbook\\\_v1.docx   # Step-by-step token deploy

│  │  ├─ OBEN\\\_Blockchain\\\_Rail\\\_Creation\\\_Runbook\\\_v1.docx  # Rail / chain setup

│  │  ├─ OBEN\\\_Hosting\\\_Platform\\\_Runbook\\\_v1.docx # Hosting / infra workflows

│  └─ diagrams/

│     ├─ TBD\\\_hex\\\_lattice\\\_global.png            # (to be added) Hex node lattice

│     ├─ TBD\\\_one\\\_line\\\_power\\\_model.png          # (to be added) power / current 1-line

│     ├─ TBD\\\_1H\\\_lattice\\\_zoom.png               # (to be added) 1H ice / spin mapping

│     ├─ TBD\\\_global\\\_EMF\\\_belts.png              # (to be added) global EM field analog

├─ contracts/

│  ├─ tokens/

│  │  ├─ LibraToken.sol                        # ERC-20 (or ERC-20 + extensions)

│  │  ├─ LithiumToken.sol

│  │  ├─ OrionToken.sol

│  ├─ rails/

│  │  ├─ LibraRail.sol                         # Chain config / router wrappers

│  │  ├─ LithiumRail.sol

│  │  ├─ OrionRail.sol

│  └─ governance/

│     ├─ ObenGovernor.sol                      # (future) on-chain governance

│     ├─ ObenTimelock.sol

├─ infrastructure/

│  ├─ aws/

│  │  ├─ aws\\\_state\\\_snapshot.md                 # Which EC2 nodes exist + region

│  │  ├─ aws\\\_tagging\\\_conventions.md            # Stage / Role / Hemisphere / PoleRole

│  │  ├─ terraform/                            # (future) infra-as-code if desired

│  ├─ wallet\\\_config/

│  │  ├─ wallets\\\_public.md                     # Only PUBLIC addrs + roles

│  │  └─ networks.json                         # RPC URLs (Infura, etc.) – NO secrets

├─ scripts/

│  ├─ deploy/

│  │  ├─ deploy\\\_libra.js                       # Hardhat/Foundry script (future)

│  │  ├─ deploy\\\_lithium.js

│  │  ├─ deploy\\\_orion.js

│  ├─ utils/

│  │  ├─ verify\\\_contracts.js                   # Etherscan / block explorer verify helper

└─ .gitignore                                  # Ignore secrets, build artifacts, etc.




