# Beach Swimmer Safety AI & Sensor Review

<!--[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)-->
[![Paper](https://img.shields.io/badge/Paper-PDF-red.svg)](link-to-your-paper)
[![Dataset](https://img.shields.io/badge/Datasets-10+-blue.svg)](#datasets)

> **A Systematic Review of Artificial Intelligence and Sensor Technologies for Swimmer Safety in Beach Environments**

This repository contains the supplementary materials, curated datasets, and organized bibliography for our systematic review paper examining AI-driven drowning detection and swimmer safety technologies.

📅 Last update on 5 Nov 2025
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

We conducted systematic searches across multiple academic databases (IEEE Xplore, ACM Digital Library, Scopus, Google Scholar, Web of Science, and PubMed) using the following comprehensive query:

```
("swim*" OR "drown*" OR "person in water" OR "marine rescue")
AND ("*stress" OR "distress detection" OR "drowning detection" 
     OR "near-drowning" OR "search and rescue")
AND ("ocean*" OR "sea*" OR "open water" OR "beach*" OR "coastal")
AND ("AI" OR "artificial intelligence" OR "machine learning" 
     OR "deep learning" OR "computer vision" OR "image processing" 
     OR "video analytics")
AND ("wearable*" OR "sensor*" OR "smart device*" OR "UAV*" OR "drone*")
AND NOT ("pool*" OR "swimming pool*")
```

#### Supplementary Targeted Queries

To ensure comprehensive coverage, we executed six specialized queries focusing on different aspects of the research domain:

1. **Query 1 - General Drowning Detection in Ocean Contexts:**
   ```
   "drowning detection" AND (ocean OR sea OR beach) 
   AND ("deep learning" OR "AI") -"swimming pool"
   ```

2. **Query 2 - Marine Rescue with AI and Sensors:**
   ```
   "marine rescue" AND ("computer vision" OR "sensor") 
   AND (coastal OR "open water") -"swimming pool"
   ```

3. **Query 3 - Person in Water + Distress + Wearable Devices:**
   ```
   "person in water" AND ("distress detection" OR stress) 
   AND (wearable OR "smart device") -"swimming pool"
   ```

4. **Query 4 - Drowning or Near-Drowning + AI + Video Analytics:**
   ```
   (drowning OR "near-drowning") AND ("video analytics" OR "deep learning") 
   AND ocean -"swimming pool"
   ```

5. **Query 5 - Search and Rescue in Beach Environments:**
   ```
   "stress detection" AND ("open water" OR sea) 
   AND ("smart device" OR wearable) -"swimming pool"
   ```

6. **Query 6 - AI + Image Processing + Swimmer Safety:**
   ```
   "swimmer safety" AND ("image processing" OR "computer vision") 
   AND AI -"swimming pool"
   ```

### Categories
1. **Vision-Based AI Systems** (45 papers)
   - Object detection (YOLO, Faster R-CNN, SSD)
   - Semantic segmentation
   - Activity recognition

  | Paper | Published in |
|-------|:------------:|
| [SeaDronesSee: A Maritime Benchmark for Detecting Humans in Open Water](https://openaccess.thecvf.com/content/WACV2022/html/Varga_Seadronessee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) | WACV 2022 |
| [MOBDrone: Drone Video Dataset for Man-Overboard Rescue](http://aimh.isti.cnr.it/dataset/MOBDrone) | arXiv 2022 |
| [Outdoor Swimmers Detection System with Small Object Detection](https://doi.org/10.1007/s00530-022-00995-7) | Multimedia Systems 2022 |
| [MS-YOLO: Lightweight YOLO Model for Drowning Detection](https://doi.org/10.3390/s24216955) | Sensors 2024 |
| [DeepDASH: Swimmer Detection, Tracking & Action Localization](https://doi.org/10.1007/s00521-020-05485-3) | Neural Computing & Applications 2020 |
| [Smart Multi-Sensor Drowning Detection Device](https://doi.org/10.1109/jsen.2024.3518436) | IEEE Sensors Journal 2025 |
| [Technological Approaches for Drowning Detection – Review](https://doi.org/10.3390/s24020331) | Sensors 2024 |
| [Automated Drowning Detection Review & Challenges](https://www.mdpi.com/2078-2489/15/11/721) | Information 2024 |
| [Dataset Rebalancing for Drone Maritime Rescue](https://doi.org/10.1007/s00371-025-04098-y) | The Visual Computer 2025 |
| [AI-Powered Swimming Pool Drowning Prevention with IoT](https://doi.org/10.1016/j.heliyon.2024.e35484) | Heliyon 2024 |
| [Infant Drowning Detection using YOLOv5 & Faster-RCNN](https://doi.org/10.23919/JSC.2023.0006) | Journal of Social Computing 2023 |
| [Video Drowning Detection on Jetson with CNN](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/ipr2.12765) | IET Image Processing 2023 |
| [3D CNN-LSTM Foreground Segmentation](https://doi.org/10.1109/TITS.2019.2900426) | IEEE T-ITS 2020 |
| [Mask-Refined R-CNN for Instance Segmentation](https://doi.org/10.3390/s20041010) | Sensors 2020 |
| [Lightweight Outdoor Drowning Detection via YOLOv8](https://doi.org/10.1007/s11554-025-01638-6) | JRTIP 2025 |
| [Generative AI for Drowning Scene Dataset Generation](https://doi.org/10.1109/ACCESS.2024.3407245) | IEEE Access 2024 |
| [Real-time UAV Beach Monitoring with CV](https://doi.org/10.1109/ROBOT61475.2024.10797412) | Iberian Robotics Conf. 2024 |
| [Drone + ML Recognition of Simulated Drowning Victims](https://www.sciencedirect.com/science/article/pii/S0300957220304706) | Resuscitation 2020 |
| [Synthetic Data for Maritime Body Detection](https://doi.org/10.1016/j.engappai.2024.109586) | Engineering Applications of AI 2025 |
| [Drowning Behavior Detection in Swimming Pool](https://doi.org/10.1007/s11760-021-02124-9) | SIVP 2022 |
| [Swimming-YOLO: Drowning Detection in Multiple Swimmers](https://doi.org/10.1007/s11760-024-03744-7) | SIVP 2024 |
| [Unsupervised Human Detection on UAVs (Lygouras)](https://doi.org/10.3390/s19163542) | Sensors 2019 |
| [Drone-Based Water Rescue Ensemble Detection](https://doi.org/10.3233/ICA-210649) | ICAE 2021 |
| [TinyPerson Benchmark for Tiny Object Detection](https://openaccess.thecvf.com/content/WACV2020/html/Yu_Scale_Match_for_Tiny_Person_Detection_WACV_2020_paper.html) | WACV 2020 |
| [Synthetic Maritime Victim Imagery via UAV Sim](https://doi.org/10.1109/ICCE48956.2021.9352109) | ICCE 2021 |
| [Leveraging Synthetic Data for UAV Detection](https://arxiv.org/abs/2112.12252) | arXiv 2021 |
| [RipVIS: Rip Currents Segmentation Benchmark](https://arxiv.org/abs/2504.01128) | arXiv 2025 |
| [Automated Rip Current Detection with R-CNN](https://arxiv.org/abs/2102.02902) | arXiv 2021 |


2. **Sensor-Based Systems** (38 papers)
   - Wearable technologies
   - Acoustic and environmental sensors
   - Communication protocols

| Paper | Published in |
|-------|:------------:|
| [Smart Multi-Sensor Device to Detect Distress in Swimmers](https://doi.org/10.3390/s22031059) | Sensors 2022 |
| [AI-Based Smart Surveillance for Drowning & Theft Detection on Beaches](https://doi.org/10.1002/9781394168002.ch10) | Wiley Book Chapter 2023 |
| [Wearables in Swimming for Real-Time Feedback: Systematic Review](https://doi.org/10.3390/s22103677) | Sensors 2022 |
| [Automated Wearable Device to Detect Drowning Incidents](https://doi.org/10.1109/ICAIT61638.2024.10690678) | ICAIT 2024 |
| [A Portable Wearable Blood-Oxygen Sensor for Swimming Safety](https://doi.org/10.3390/s22103823) | Sensors 2022 |
| [Smart Multi-Sensor Drowning Detection Device With Real-Time Alarm](https://doi.org/10.1109/jsen.2024.3518436) | IEEE Sensors Journal 2025 |
| [A Smart Multi-Sensor Device to Detect Distress in Swimmers](https://doi.org/10.3390/s22031059) | Sensors 2022 |
| [Enhancing Water Safety: Tech Approaches for Drowning Detection](https://doi.org/10.3390/s24020331) | Sensors 2024 |
| [Advances & Challenges in Drowning Detection Systems](https://www.mdpi.com/2078-2489/15/11/721) | Information 2024 |
| [Novel Drowning Detection System Using IoT & Sensors](https://doi.org/10.1109/NPSC.2018.8771844) | NPSC 2018 |
| [Connected Wearable Sensors for Swimming Analytics](https://doi.org/10.3390/s21155162) | Sensors 2021 |
| [Low-Power Underwater Wireless Sensor Network Design](https://doi.org/10.3390/s22041618) | Sensors 2022 |
| [Underwater Wireless Sensor Networks Review](https://doi.org/10.12928/TELKOMNIKA.v21i3.24010) | TELKOMNIKA 2023 |
| [Sonar-Based Swimmer Location Monitor](https://doi.org/10.1121/1.1492881) | JASA 2002 |
| [Thermal & Radar Systems for Maritime Rescue](https://doi.org/10.1364/OE.15.012296) | Optics Express 2007 |
| [Distributed Acoustic Sensing for Ocean Applications](https://doi.org/10.58046/5J60-FJ89) | 2025 |
| [Drone Relay for Swimmer Distress Response](https://doi.org/10.1109/ARGENCON49523.2020.9505478) | IEEE ARGENTCON 2020 |
| [Wearable Pulse-Oximeter for Pool Safety](https://doi.org/10.3390/s22103823) | Sensors 2022 |
| [Triboelectric Self-Powered Drowning Sensor](https://doi.org/10.1016/j.nanoen.2021.106835) | Nano Energy 2022 |
| [Self-Powered ZnO Biosensor for Underwater Motion](https://doi.org/10.3390/bios11050147) | Biosensors 2021 |
| [Anti-Swelling Hydrogel Strain Sensor](https://doi.org/10.1002/adfm.202107404) | Advanced Functional Materials 2021 |
| [Carbon Fiber Strain Sensor for Underwater Respiration](https://doi.org/10.1016/j.apmt.2024.102165) | Applied Materials Today 2024 |
| [Amphibian-Inspired Ionogel Sensor for Swimmer Motion](https://github.com/ucas-vg/PointTinyBenchmark) | 2024 |
| [Superhydrophobic Fabric Sensor for Water Motion](https://doi.org/10.1021/acsnano.2c08325) | ACS Nano 2022 |
| [Energy-Optimized Routing for UWSN Sensor Nodes](https://doi.org/10.3390/s22041618) | Sensors 2022 |
| [Energy-Aware Clustering in UWSNs](https://doi.org/10.1016/j.scitotenv.2023.165818) | STOTEN 2023 |
| [Buoy-Based Sensor Noise & Stability Issues in Marine Sensing](https://doi.org/10.12928/TELKOMNIKA.v21i3.24010) | TELKOMNIKA 2023 |

3. **Integrated Multi-Modal Approaches** (32 papers)
   - AI-IoT integration
   - Multi-sensor data fusion
   - Drone-based surveillance

| Paper | Published in |
|-------|:------------:|
| [SharkEye: Real-Time Autonomous Shark Alerting via Aerial Surveillance](https://doi.org/10.3390/DRONES4020018) | Drones 2020 |
| [SeaDronesSee: Maritime Benchmark for Detecting Humans in Open Water](https://wacv2022.thecvf.com/) | WACV 2022 |
| [MOBDrone: Drone Video Dataset for Man-Overboard Rescue](http://aimh.isti.cnr.it/dataset/MOBDrone) | arXiv 2022 |
| [Smart Multi-Sensor Device to Detect Distress in Swimmers](https://www.mdpi.com/1424-8220/22/3/1059) | Sensors 2022 |
| [Smart Cameras + 5G for Safe Coastal Areas](https://doi.org/10.1109/MVT.2017.2753540) | IEEE Vehicular Tech Mag 2017 |
| [Smart Drowning Detection via RSSI Zigbee](https://doi.org/10.2991/978-94-6463-718-2_158) | ICSICE 2025 |
| [Robust IoT System for Smart Beaches](https://doi.org/10.1016/j.iot.2024.101295) | Internet of Things 2024 |
| [Automated Pool Safety with IoT & Transfer Learning](https://doi.org/10.3390/electronics9122082) | Electronics 2020 |
| [Enhancing Water Safety: New Technologies for Drowning Detection](https://doi.org/10.3390/s24020331) | Sensors 2024 |
| [Next-Gen Drowning Prevention (AI + IoT)](https://doi.org/10.1016/j.heliyon.2024.e35484) | Heliyon 2024 |
| [Real-Time Beach Monitoring Using UAVs & Vision](https://doi.org/10.1109/ROBOT61475.2024.10797412) | ROBOT 2024 |
| [DGTA-SeaDronesSee: Synthetic Data for UAV Detection](https://arxiv.org/abs/2112.12252) | arXiv 2021 |
| [SynBASe: Synthetic Data for Swimmer Detection](https://doi.org/10.1016/j.engappai.2025.109586) | Eng. App. of AI 2025 |
| [RipVIS: Rip Currents Video Benchmark](https://arxiv.org/abs/2504.01128) | arXiv 2025 |
| [SeaPerson: Tiny-Person Detection Dataset](https://github.com/ucas-vg/PointTinyBenchmark) | Dataset 2022 |
| [Sonar Swimmer Location Monitor](https://doi.org/10.1121/1.1492881) | JASA 2002 |
| [AquaSense Wearable AI System](https://doi.org/10.1002/ett.70081) | Emerging Telecom Tech 2025 |
| [Swimmer Safety Alert System (Marine Threats)](https://doi.org/10.55524/ijircst.2024.12.4.8) | IJIRCST 2024 |
| [Data Fusion Accuracy Prediction](https://doi.org/10.3390/s21217007) | Sensors 2021 |
| [Cloud + AI for Swimmer Movement](https://doi.org/10.1007/s11036-023-02167-x) | Mobile Net & Apps 2023 |
| [Unsupervised Multi-Source Fusion](https://doi.org/10.1016/j.inffus.2021.10.017) | Information Fusion 2022 |
| [Real-Time Multi-Sensor Tracking](https://doi.org/10.3390/pr11020501) | Processes 2023 |
| [Wearable Swimming Analysis Framework](https://doi.org/10.3390/s21155162) | Sensors 2021 |
| [Beach Water Quality Ensemble Models](https://doi.org/10.1016/j.scitotenv.2020.142760) | STOTEN 2021 |
| [Rip Current ML Vulnerability Model](https://doi.org/10.1016/j.rineng.2023.101704) | Results in Eng. 2024 |
| [SOSeas: Drowning Risk Prediction Tool](https://doi.org/10.1080/1755876X.2021.1999107) | J. Operational Oceanography 2021 |
| [Drone Revolution in Shark Monitoring](https://doi.org/10.3390/drones5010008) | Drones 2021 |
| [Drone Edge-AI Litter Detection System](https://doi.org/10.3390/drones8120750) | Drones 2024 |
| [UAV-Assisted 6G Smart Safety Survey](https://doi.org/10.3390/drones6070177) | Drones 2022 |

4. **Challenges & Applications** (21 papers)
   - Environmental robustness
   - Privacy and ethics
   - Regulatory frameworks

### Key Challenges & Research Gaps in Beach Safety AI

| Paper | Published in |
|-------|:------------:|
| [Water quality & environmental challenges at Mosqueiro Island beaches](https://doi.org/10.24857/rgsa.v18n3-029) | Revista de Gestão Social e Ambiental 2023 |
| [Floating & beach landing records of Sargassum beyond the Sargasso Sea](https://doi.org/10.1088/2515-7620/abd109) | Environmental Research Communications 2020 |
| [BeachLog: An interactive beach picture for multiple uses](https://doi.org/10.1016/j.marpolbul.2023.115156) | Marine Pollution Bulletin 2023 |
| [Urbanization/environmental features on sandy beach macrobenthos](https://doi.org/10.1016/j.marpolbul.2022.113962) | Marine Pollution Bulletin 2022 |
| [Beach nourishment compatibility & suitability (Tuscany, Italy)](https://doi.org/10.1016/j.marpolbul.2015.01.021) | Marine Pollution Bulletin 2015 |
| [Disability inclusion in beach precincts: Beach for all abilities](https://doi.org/10.1080/14413523.2022.2059998) | Sport Management Review 2022 |
| [Social dimension of sandy beaches via predictive modelling](https://doi.org/10.1016/j.jenvman.2018.03.006) | Journal of Environmental Management 2018 |
| [Advanced approaches for drowning detection: A review](https://doi.org/10.48084/etasr.7804) | ETASR 2024 |
| [Drowning prevention: define vs. gather evidence first?](https://doi.org/10.25035/IJARE.10.04.01) | International Journal of Aquatic Research and Education 2019 |
| [Neural network algorithms for early pool drowning detection](https://doi.org/10.1109/ICIEAM57311.2023.10139153) | IEEE ICIEAM 2023 |
| [Real-time swimmers detection with small-object DL](https://doi.org/10.1007/s00530-022-00995-7) | Multimedia Systems 2022 |
| [Outdoor swimmer localisation with YOLO: real vs. synthetic data](https://doi.org/10.3390/ai5020030) | AI (MDPI) 2024 |
| [MSRTD: Maritime search-and-rescue target dataset] | Drones (In press) 2025 |
| SeaDronesSee: Maritime benchmark for detecting humans in open water | WACV 2022 |
| [MOBDrone: Man-overboard drone video dataset](http://aimh.isti.cnr.it/dataset/MOBDrone) | arXiv/Dataset 2022 |
| [Scale Match for Tiny Person Detection](https://doi.org/10.1109/WACV45572.2020.9093394) | WACV 2020 |
| [Victims on Ocean: Synthetic UAV SAR training data](https://doi.org/10.1109/ICCE48956.2021.9352109) | IEEE ICCE 2021 |
| [Leveraging synthetic data in object detection on UAVs](https://arxiv.org/abs/2112.12252) | arXiv 2021 |
| [SynBASe: Synthetic simulated swimmer dataset](https://doi.org/10.1016/j.engappai.2025.109586) | Engineering Applications of AI 2025 |
| [RipVIS: Rip currents video instance segmentation benchmark](https://arxiv.org/abs/2504.01128) | arXiv 2025 |
| [Automated rip current detection with R-CNNs](https://www.sciencedirect.com/science/article/pii/S0378383921000193) | Coastal Engineering 2021 |
| [Smart multi-sensor device to detect distress in swimmers](https://www.mdpi.com/1424-8220/22/3/1059) | Sensors 2022 |
| [Smart multi-sensor device to detect distress in swimmers](https://doi.org/10.1109/JSEN.2021.3119977) | IEEE Sensors Journal 2022 |
| [Wearables in swimming for real-time feedback: systematic review](https://doi.org/10.3390/s22103677) | Sensors 2022 |
| [Low-cost sensors for monitoring coastal climate hazards](https://www.mdpi.com/1424-8220/23/3/1717) | Sensors 2023 |
| [Predicting best sensor fusion architecture (multi-domain)](https://doi.org/10.3390/s21217007) | Sensors 2021 |
| [Data-level fusion model for unsupervised attribute selection](https://www.sciencedirect.com/science/article/pii/S1566253521002256) | Information Fusion 2022 |
| [Multi-sensor data fusion for real-time multi-object tracking](https://doi.org/10.3390/pr11020501) | Processes 2023 |
| [Multi-sensor data fusion solutions for blind/VI navigation](https://doi.org/10.3390/s23125411) | Sensors 2023 |
| [Requirements & limitations of thermal drones for SAR](https://doi.org/10.3390/drones3040078) | Drones 2019 |
| [Drone-enabled AI edge + 5G for real-time coastal litter](https://doi.org/10.3390/drones8120750) | Drones 2024 |
| [Computing in the sky: UAV-assisted 6G survey](https://doi.org/10.3390/drones6070177) | Drones 2022 |
| [Coastal & environmental remote sensing from UAVs](https://www.jcronline.org/doi/10.2112/JCOASTRES-D-15-00005.1) | Journal of Coastal Research 2015 |
| [UAVs for coastal surveying](https://www.sciencedirect.com/science/article/pii/S0378383916300260) | Coastal Engineering 2016 |
| [Drone revolution of shark science: a review](https://doi.org/10.3390/drones5010008) | Drones 2021 |
| [Drone insights: AI people counting on beaches](https://doi.org/10.3390/drones8100579) | Drones 2024 |
| [Public beach access & environmental justice](https://doi.org/10.1111/cico.12372) | City & Community 2019 |
| [Drones, privacy and data protection] | LESIJ 2021 |
| [UAS governance & regulatory frameworks in the EU](https://www.sciencedirect.com/science/article/pii/B9780323919401000128) | Book chapter (Academic Press) 2023 |
| [Fairness & bias in AI: survey](https://doi.org/10.3390/sci6010003) | Sci 2024 |
| [World Drowning Prevention Day](https://www.who.int/campaigns/world-drowning-prevention-day) | WHO 2025 |
| [Improving coastal safety for international visitors](https://doi.org/10.1016/j.puhip.2025.100613) | Public Health in Practice 2025 |
| [Risk factors for beach drowning in a multicultural community](https://doi.org/10.1371/journal.pone.0262175) | PLOS ONE 2022 |
| [PRISMA statement: reporting systematic reviews](https://doi.org/10.1371/journal.pmed.1000100) | PLOS Medicine 2009 |


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
