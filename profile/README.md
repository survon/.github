# Survon Organization

Welcome to the Survon organization on GitHub! Survon is an offline, off-grid survival system designed to operate in challenging scenarios where reliability, modularity, and adaptability are crucial. At its core, Survon puts humanity and freedom first, fostering societal resilience and safeguarding knowledge to ensure essential tools and technology remain accessible even in the face of systemic disruptions. In a world increasingly dependent on fragile systems, Survon is a practical response to challenges like energy crises, communication breakdowns, or resource scarcity. It equips individuals and communities to adapt, innovate, and thrive. Our mission is to create a robust ecosystem that empowers users to maintain and expand their systems without requiring technical expertise.

## Repository Structure
The Survon ecosystem consists of core runtimes, field runtimes, and modular components contributed by the community. Below is an overview of the repositories:

### 1. **`runtime-base-rust`**
This repository contains the **core runtime** for Survon. It handles:
- Managing the Survon system state.
- Registering, validating, and building modules.
- Syncing updates to portable field units.
- Providing a CLI for managing modules and system updates.

#### Features:
- Module validation via metadata.
- Binary compilation and version control.
- USB-based syncing with field units.

#### Use Cases:
- Centralized management for all Survon modules.
- Ensuring system consistency before distributing updates.

[Explore `runtime-base-rust`](https://github.com/survon/runtime-base-rust)

---

### 2. **`runtime-field-rust`**
This repository contains the **field runtime**, which is a lightweight, portable system designed for use in off-grid scenarios. It focuses on:
- Running compiled Survon binaries.
- Executing modules efficiently in resource-constrained environments.
- Providing a user-friendly interface for offline use.

#### Features:
- Precompiled static binary for maximum reliability.
- Minimal resource usage for portability (e.g., Raspberry Pi).
- Plug-and-play updates from the core runtime.

#### Use Cases:
- Field-ready devices for real-world survival scenarios.
- Portable systems that don’t require Internet connectivity.

[Explore `runtime-field-rust`](https://github.com/survon/runtime-field-rust)

---

### 3. **Community Modules**
Modules are the heart of the Survon system. Each module adds specific functionality, such as communication, monitoring, or computation, ensuring adaptability in a wide range of scenarios, including post-disaster environments. Modules follow a strict packaging standard to ensure compatibility and security.

#### Module Categories and Prefixes
Modules are categorized to maintain consistency and clarity. Each category has a unique prefix used in module naming:

- **Communication (`com`)**: Modules for communication systems.
- Example: `mod-rust-com--morse-code`, `mod-rust-com--irc`
- **Monitoring (`mon`)**: Modules for monitoring systems and sensors.
- Example: `mod-rust-mon--temperature-sensor`, `mod-rust-mon--camera-feed`
- **Defense (`def`)**: Modules for defensive systems.
- Example: `mod-rust-def--manual-turret`, `mod-rust-def--motion-turret`
- **Power (`pow`)**: Modules for managing power systems.
- Example: `mod-rust-pow--solar-array`, `mod-rust-pow--battery-monitor`
- **Weather (`wth`)**: Modules for weather tracking and forecasting.
- Example: `mod-rust-wth--storm-alert`, `mod-rust-wth--rain-gauge`
- **Library (`lib`)**: Knowledge and computational modules.
- Example: `mod-rust-lib--pubmed-library`, `mod-rust-lib--math-utils`
- **Agriculture (`agr`)**: Modules for farming and food production.
- Example: `mod-rust-agr--soil-monitor`, `mod-rust-agr--irrigation-control`
- **Entertainment (`ent`)**: Modules for recreational activities.
- Example: `mod-rust-ent--text-adventure`, `mod-rust-ent--media-player`
- **Crafting (`crf`)**: Modules for creating or repairing items.
- Example: `mod-rust-crf--blueprint-helper`, `mod-rust-crf--tool-fabricator`
- **Electronics (`ele`)**: Modules for electronics design and control.
- Example: `mod-rust-ele--circuit-simulator`, `mod-rust-ele--signal-generator`
- **Sensors (`sen`)**: Modules for sensor integration.
- Example: `mod-rust-sen--motion-detector`, `mod-rust-sen--proximity-sensor`
- **Traps (`trp`)**: Modules for trapping and detection systems.
- Example: `mod-rust-trp--animal-trap`, `mod-rust-trp--intruder-alarm`

#### Example Modules:
- **`mod-rust-com--morse-code`**: Provides functionality for encoding and decoding Morse code.
- **`mod-rust-com--irc`**: Enables communication via IRC networks.

#### Community Contribution Guidelines:
Each module must:
1. Be packaged as a zip file containing:
- `meta.json`: Metadata for validation.
- Module source code (e.g., `mod.rs` or `module.rs`).
- Optional files: `README.md`, `LICENSE`, `tests/`.
2. Include a `README.md` describing:
- Module purpose and functionality.
- Installation instructions.
- Examples of use.
3. Follow semantic versioning.
4. Pass all required tests.

---

## Getting Started
1. Clone the **runtime-base-rust** repository and set up the core runtime.
```bash
git clone https://github.com/survon/runtime-base-rust.git
cd runtime-base-rust
cargo build
```

2. Explore example modules and add them to your runtime:
```bash
survon-core add-module https://example.com/modules/mod-rust-com--morse-code.zip
survon-core build
```

3. Sync updates to a field device:
```bash
survon-core sync /path/to/usb_device
```

---

## Contribution Guidelines
We welcome contributions from the community! Please follow these steps:
1. Fork the appropriate repository.
2. Create a branch for your changes.
3. Submit a pull request with detailed explanations.

For module contributions, ensure you follow the [Module Packaging Standards](#community-modules).

---

## License
All repositories are open-source and released under the [MIT License](LICENSE). Contributions to the repositories must adhere to this license.

---

## Contact
For questions, suggestions, or discussions, please open an issue in the relevant repository or reach out to the maintainers via GitHub Discussions.

---

Let’s build a resilient, modular, and community-driven survival system together!
