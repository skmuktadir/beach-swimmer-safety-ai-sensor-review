# beach-swimmer-safety-ai-sensor-review
A systematic review of AI and sensor technologies for swimmer safety and drowning detection in beach environments. Includes curated datasets, 136+ papers, and comprehensive taxonomy of detection systems.

# Beach Swimmer Safety AI & Sensor Review

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Paper](https://img.shields.io/badge/Paper-PDF-red.svg)](link-to-your-paper)
[![Dataset](https://img.shields.io/badge/Datasets-10+-blue.svg)](#datasets)

> **A Systematic Review of Artificial Intelligence and Sensor Technologies for Swimmer Safety in Beach Environments**

This repository contains the supplementary materials, curated datasets, and organized bibliography for our systematic review paper examining AI-driven drowning detection and swimmer safety technologies.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Contributions](#key-contributions)
- [Repository Structure](#repository-structure)
- [Datasets](#datasets)
- [Paper Collection](#paper-collection)
- [Taxonomy](#taxonomy)
- [Getting Started](#getting-started)
- [Citation](#citation)
- [Contact](#contact)
- [License](#license)

---

## 🌊 Overview

Drowning is one of the ten leading causes of unintentional injury-related death worldwide, with an estimated **236,000 fatalities annually**. This systematic review examines how artificial intelligence, computer vision, wearable sensors, and IoT technologies can enhance beach safety and prevent drowning incidents.

### Scope
- **136 peer-reviewed studies** analyzed (PRISMA-compliant)
- **Vision-based systems**: YOLO, CNN, UAV surveillance
- **Sensor-based systems**: Wearables, IMU, SpO₂, environmental sensors
- **Multi-modal approaches**: Integrated AI-IoT platforms

### Research Questions
1. What AI and sensor technologies are effective for swimmer danger detection?
2. What are the performance metrics and deployment constraints?
3. What datasets are publicly available for research?
4. What are the key challenges and future research directions?

---

## 🎯 Key Contributions

1. **Unified Taxonomy**: Comprehensive classification of beach safety technologies into three tiers:
   - Vision-centric systems (fixed and aerial surveillance)
   - Swimmer-centric wearables (physiological and kinematic sensors)
   - Integrated cyber-physical platforms

2. **Curated Dataset Catalog**: First comprehensive checklist of **10+ publicly available beach safety datasets**
   - Includes SeaDronesSee, MOBDrone, RipVIS, TinyPerson, and more
   - Detailed annotations, geographic diversity, and licensing information

3. **Research Roadmap**: Identifies critical gaps and proposes directions:
   - Domain-adaptive learning for cross-beach generalization
   - Energy-aware neural architectures
   - Privacy-preserving inference pipelines
   - Human-in-the-loop system design

4. **Performance Benchmarks**: Synthesized metrics across 136 studies
   - Detection accuracy, latency, computational efficiency
   - Real-world deployment constraints

---

## 📁 Repository Structure

```
beach-swimmer-safety-ai-sensor-review/
│
├── README.md                          # This file
├── LICENSE                            # MIT License
│
├── paper/
│   ├── main_paper.pdf                # Full systematic review paper
│   ├── supplementary_materials.pdf   # Additional tables and figures
│   └── bibtex.bib                    # BibTeX citations
│
├── datasets/
│   ├── README.md                     # Dataset catalog overview
│   ├── dataset_table.csv             # Structured dataset information
│   ├── vision_datasets/              # Vision-based datasets
│   │   ├── SeaDronesSee.md
│   │   ├── MOBDrone.md
│   │   ├── RipVIS.md
│   │   └── ...
│   └── sensor_datasets/              # Sensor-based datasets
│       └── wearable_sensors.md
│
├── papers/
│   ├── bibliography.bib              # All 136 papers (BibTeX)
│   ├── papers_by_category.md         # Organized by approach
│   ├── vision_based/                 # Vision system papers
│   ├── sensor_based/                 # Sensor system papers
│   └── multimodal/                   # Integrated approaches
│
├── taxonomy/
│   ├── taxonomy_diagram.png          # Visual representation
│   └── taxonomy_description.md       # Detailed explanation
│
├── figures/
│   ├── prisma_flow.png               # PRISMA flow diagram
│   ├── beach_hazards.png             # Beach hazard illustration
│   └── workflow.png                  # Research workflow
│
└── scripts/
    ├── data_analysis.py              # Bibliometric analysis scripts
    └── visualization.py              # Generate charts and graphs
```

---

## 📊 Datasets

### Vision-Based Datasets

| Dataset | Year | Type | Annotations | Application | Public |
|---------|------|------|-------------|-------------|--------|
| [SeaDronesSee](https://seadronessee.cs.uni-tuebingen.de/) | 2022 | UAV Video/Image | BBox: swimmer, floater, life-jacket | Distress detection | ✅ |
| [MOBDrone](http://aimh.isti.cnr.it/dataset/MOBDrone) | 2022 | UAV Video/Image | BBox: person, boat, lifebuoy | Man-overboard | ✅ |
| [RipVIS](https://github.com/andreeadeac22/rip_current_dataset) | 2025 | Multi-view Video | Polygon masks: rip currents | Rip current detection | ✅ |
| [TinyPerson](https://github.com/ucas-vg/TinyPerson) | 2020 | Drone/Web Image | BBox: tiny persons | SAR operations | ✅ |
| [AFO](https://github.com/HadiFarhat/Floating-Object-Detection) | 2021 | UAV Image | BBox: floating objects | Search and rescue | ✅ |

[**➜ Full Dataset Catalog**](datasets/README.md)

### Sensor-Based Systems

- **Wearable Sensors**: IMU, accelerometer, SpO₂, heart rate, depth sensors
- **Environmental Sensors**: Sonar, thermal imaging, radar, LiDAR
- **Communication**: LoRa, BLE, NB-IoT, GPS

---

## 📚 Paper Collection

Our systematic review analyzed **136 peer-reviewed studies** following PRISMA methodology:

### Search Process
- **Initial records**: 2,727 papers
- **After screening**: 2,183 papers
- **Final inclusion**: 136 papers

### Categories
1. **Vision-Based AI Systems** (45 papers)
   - Object detection (YOLO, Faster R-CNN, SSD)
   - Semantic segmentation
   - Activity recognition

2. **Sensor-Based Systems** (38 papers)
   - Wearable technologies
   - Acoustic and environmental sensors
   - Communication protocols

3. **Integrated Multi-Modal Approaches** (32 papers)
   - AI-IoT integration
   - Multi-sensor data fusion
   - Drone-based surveillance

4. **Challenges & Applications** (21 papers)
   - Environmental robustness
   - Privacy and ethics
   - Regulatory frameworks

[**➜ Full Bibliography**](papers/bibliography.bib)

---

## 🏗️ Taxonomy

Our unified taxonomy organizes beach safety technologies into three main categories:

### 1. Vision-Based Systems
- **Fixed Surveillance**: CCTV, beach cameras
- **UAV-Based**: Drones, aerial monitoring
- **AI Models**: CNN, YOLO variants, semantic segmentation

### 2. Sensor-Based Systems
- **Wearables**: IMU, heart rate, SpO₂, depth sensors
- **Environmental**: Sonar, thermal, radar, water quality
- **Communication**: LoRa, BLE, GPS, cellular

### 3. Multi-Modal Systems
- **Vision + Sensor Fusion**: Combined approaches
- **Edge/Cloud AI**: Distributed architectures
- **Adaptive Response**: Human-in-the-loop systems

![Taxonomy Diagram](taxonomy/taxonomy_diagram.png)

[**➜ Detailed Taxonomy**](taxonomy/taxonomy_description.md)

---

## 🚀 Getting Started

### Prerequisites
```bash
# Clone the repository
git clone https://github.com/yourusername/beach-swimmer-safety-ai-sensor-review.git
cd beach-swimmer-safety-ai-sensor-review
```

### Explore the Dataset Catalog
```bash
cd datasets
cat README.md
```

### Access the Bibliography
```bash
# All papers in BibTeX format
cat papers/bibliography.bib

# Papers organized by category
cat papers/papers_by_category.md
```

### Run Analysis Scripts (Optional)
```bash
# Install dependencies
pip install -r requirements.txt

# Run bibliometric analysis
python scripts/data_analysis.py

# Generate visualizations
python scripts/visualization.py
```

---

## 📖 Citation

If you use this work in your research, please cite:

```bibtex
@article{yoursurname2025swimmer,
  title={Artificial Intelligence and Sensor Technologies for Swimmer Safety in Beach Environments: A Systematic Review},
  author={Your Name and Co-authors},
  journal={Journal Name},
  year={2025},
  volume={XX},
  pages={XX-XX},
  doi={XX.XXXX/XXXXX}
}
```

**Paper**: [Link to published paper](#) (Coming soon)

---

## 🔬 Research Gaps Identified

1. **Dataset Scarcity**: Only 10 public datasets, no multi-sensor fusion datasets
2. **Model Transferability**: Limited cross-beach generalization studies
3. **End-to-End Integration**: Gap between AI detection and rescue actuation
4. **Privacy & Ethics**: Need for privacy-preserving architectures

---

## 🛣️ Future Research Directions

### Priority Areas
- [ ] Open multi-modal datasets with synchronized sensors
- [ ] Edge AI optimization for real-time processing
- [ ] Climate-aware adaptive AI systems
- [ ] Privacy-preserving on-device inference
- [ ] Human-AI collaboration interfaces
- [ ] Standardized benchmarking protocols

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md).

### How to Contribute
1. **Add datasets**: Submit pull requests with new dataset information
2. **Update papers**: Suggest additional relevant papers
3. **Report issues**: Found an error? Open an issue
4. **Improve documentation**: Help us make this resource better

---

## 👥 Authors

- **Your Name** - *Lead Author* - [University/Institution]
- **Co-author 1** - [University/Institution]
- **Co-author 2** - [University/Institution]

### Corresponding Author
📧 Email: your.email@institution.edu

---

## 🙏 Acknowledgments

- All authors of the 136 papers reviewed
- Dataset creators who made their work publicly available
- Reviewers and contributors to this project
- [Funding sources, if any]

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Paper Copyright
The paper content is © 2025 [Authors]. Please cite appropriately.

---

## 📞 Contact

For questions, suggestions, or collaboration opportunities:

- **Email**: your.email@institution.edu
- **Issues**: [GitHub Issues](https://github.com/yourusername/beach-swimmer-safety-ai-sensor-review/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/beach-swimmer-safety-ai-sensor-review/discussions)

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/beach-swimmer-safety-ai-sensor-review&type=Date)](https://star-history.com/#yourusername/beach-swimmer-safety-ai-sensor-review&Date)

---

## 📈 Statistics

- **Papers Analyzed**: 136
- **Public Datasets**: 10+
- **Years Covered**: 2013-2025
- **Countries Represented**: 25+
- **Technologies Reviewed**: Vision AI, IoT, Wearables, UAVs

---

**Last Updated**: November 2025

**Repository Status**: 🟢 Active Maintenance

---

*Making beaches safer through AI and sensor technologies* 🏖️🤖
