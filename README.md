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
|-------|--------------|
| [CCTV-Based Swimmer Detection and Rip Current Monitoring](https://doi.org/10.2112/SI72-007.1) | Journal of Coastal Research 2014 |
| [Video-Based Drowning Detection with Active Contours](https://www.mecs-press.org/ijigsp/ijigsp-v6-n1/IJIGSP-V6-N1-1.pdf) | IJIGSP 2014 |
| [Neural Network-Based Drowning Detection in Coastal Lines](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6910967/) | Journal of Injury and Violence Research 2019 |
| [3D CNN-LSTM for Foreground Segmentation](https://doi.org/10.1109/TITS.2019.2900426) | IEEE T-ITS 2020 |
| [DeepDASH: Swimmer Detection, Tracking & Action Localization](https://doi.org/10.1007/s00521-020-05485-3) | Neural Computing & Applications 2020 |
| [Drone-Based Shark Detection with Machine Learning](https://doi.org/10.3390/DRONES4020018) | Drones 2020 |
| [Drones & ML for Simulated Drowning Victim Recognition](https://doi.org/10.1016/j.resuscitation.2020.09.022) | Resuscitation 2020 |
| [Mask-Refined R-CNN for Instance Segmentation](https://doi.org/10.3390/s20041010) | Sensors 2020 |
| [TinyPerson: Tiny Person Detection Dataset](https://doi.org/10.1109/WACV45572.2020.9093394) | WACV 2020 |
| [Automated Rip Current Detection with F-RCNN](https://doi.org/10.1016/j.coastaleng.2021.103859) | Coastal Engineering 2021 |
| [Aerial Floating Objects (AFO) Dataset](https://doi.org/10.3233/ICA-210649) | Integrated Computer-Aided Engineering 2021 |
| [DGTA-SeaDronesSee: Synthetic Pre-training Dataset](https://arxiv.org/abs/2112.12252) | arXiv 2021 |
| [Victims on Ocean: Synthetic Victim Detection](https://doi.org/10.1109/ICCE48956.2021.9352109) | IEEE ICCE 2021 |
| [Outdoor Swimmers Detection with Small Object Detection](https://doi.org/10.1007/s00530-022-00995-7) | Multimedia Systems 2022 |
| [YOLO-Rip: Modified Lightweight Network for Rip Currents](https://doi.org/10.3389/fmars.2022.930478) | Frontiers in Marine Science 2022 |
| [Early Drowning Detection in Deep Water using YOLOv3](https://doi.org/10.1007/s11760-021-01953-y) | SIViP 2022 |
| [BR-YOLOv4: Behavior Recognition for Drowning](https://doi.org/10.1007/s11760-021-02124-9) | SIViP 2022 |
| [Swimming Stroke Recognition with IMUs](https://doi.org/10.1080/01691864.2022.2160274) | Advanced Robotics 2022 |
| [Automatic Swimming Activity Recognition with Single IMU](https://doi.org/10.3390/s22155786) | Sensors 2022 |
| [SeaDronesSee Benchmark](https://openaccess.thecvf.com/content/WACV2022/html/Varga_Seadronessee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html) | WACV 2022 |
| [MOBDrone Dataset](http://aimh.isti.cnr.it/dataset/MOBDrone) | arXiv 2022 |
| [Convolutional Autoencoder for Drowning Anomaly Detection](https://doi.org/10.1007/s00521-023-08526-9) | Neural Computing & Applications 2023 |
| [Underwater CV Drowning Detection Device](https://doi.org/10.1049/ipr2.12765) | IET Image Processing 2023 |
| [MS-YOLO: Lightweight YOLO for Drowning](https://doi.org/10.3390/s24216955) | Sensors 2024 |
| [Swimming-YOLO: Multi-Scenario Drowning Detection](https://doi.org/10.1007/s11760-024-03744-7) | SIViP 2024 |
| [AI-Driven Beach Usage Monitoring with Drones](https://doi.org/10.3390/drones8100579) | Drones 2024 |
| [Generative AI for Drowning Warning (Dataset)](https://doi.org/10.1109/ACCESS.2024.3407245) | IEEE Access 2024 |
| [Real-Time Beach Monitoring with UAVs](https://doi.org/10.1109/ROBOT61475.2024.10797412) | Iberian Robotics Conference 2024 |
| [Investigating Real vs Synthetic Training Data for YOLO](https://doi.org/10.3390/ai5020030) | AI Journal 2024 |
| [Coastal Litter Detection with Drones & 5G](https://doi.org/10.3390/drones8120750) | Drones 2024 |
| [Lightweight YOLOv8 Outdoor Drowning Detection](https://doi.org/10.1007/s11554-025-01638-6) | JRTIP 2025 |
| [Dataset Rebalancing for UAV Maritime Rescue](https://doi.org/10.1007/s00371-025-04098-y) | The Visual Computer 2025 |
| [RipVIS: Rip Current Video Instance Segmentation](https://arxiv.org/abs/2504.01128) | arXiv 2025 |
| [SynBASe: Synthetic Data for Maritime SAR](https://doi.org/10.1016/j.engappai.2024.109586) | Engineering Applications of AI 2025 |


2. **Sensor-Based Systems** (38 papers)
   - Wearable technologies
   - Acoustic and environmental sensors
   - Communication protocols

| Paper | Published in |
|-------|--------------|
| [Goggle-Based Drowning Detection with Arduino](https://doi.org/10.12733/jcis7332) | J. Computational Information Systems 2013 |
| [Early Monitoring Device with SpO₂ & Depth](https://doi.org/10.12733/jcis7332) | J. Computational Information Systems 2013 |
| [Sonar Swimmer Location Monitor](https://doi.org/10.1121/1.1492881) | JASA 2002 |
| [Portable Self-Powered Multi-Functional Sensor](https://doi.org/10.3390/bios11050147) | Biosensors 2021 |
| [Self-Powered ZnO Biosensor](https://doi.org/10.3390/bios11050147) | Biosensors 2021 |
| [Anti-Swelling Hydrogel Strain Sensor](https://doi.org/10.1002/adfm.202107404) | Advanced Functional Materials 2021 |
| [Waterproof Multi-Sensor Device for Swimmers](https://www.mdpi.com/1424-8220/22/3/1059) | Sensors 2022 |
| [Wearable Pulse Oximeter for Drowning Detection](https://doi.org/10.3390/s22103823) | Sensors 2022 |
| [Amphibian-Inspired Ionogel Sensor](https://doi.org/10.3390/s22103823) | Sensors 2022 |
| [Triboelectric Nanogenerator for Drowning Detection](https://doi.org/10.1016/j.nanoen.2021.106835) | Nano Energy 2022 |
| [IMU-Based Swimming Stroke Recognition](https://doi.org/10.1080/01691864.2022.2160274) | Advanced Robotics 2022 |
| [Single IMU Swimming Activity Recognition](https://doi.org/10.3390/s22155786) | Sensors 2022 |
| [Wearable Sensors for Swimming Performance](https://doi.org/10.3390/s22103677) | Sensors 2022 |
| [Wireless Sensor Networks for Marine Monitoring](https://doi.org/10.3390/s22041618) | Sensors 2022 |
| [Energy-Optimized Routing for UWSNs](https://doi.org/10.3390/s22041618) | Sensors 2022 |
| [Superhydrophobic Fabric Sensor with Bluetooth](https://doi.org/10.1021/acsnano.2c08325) | ACS Nano 2022 |
| [Breathable Knitted Fabric Smart System](https://doi.org/10.1021/acsnano.2c08325) | ACS Nano 2022 |
| [Wearable Drowning Detection Prototype](https://doi.org/10.1109/ICAIT61638.2024.10690678) | ICAIT 2024 |
| [LoRa-Based Wearable for Vital Sign Monitoring](https://doi.org/10.1109/PICom64201.2024.00033) | IEEE PICom 2024 |
| [Carbon Fiber Strain Sensor for Respiration](https://doi.org/10.1016/j.apmt.2024.102165) | Applied Materials Today 2024 |
| [Corrugated Carbon Fiber Strain Sensors](https://doi.org/10.1016/j.apmt.2024.102165) | Applied Materials Today 2024 |
| [Smart Multi-Sensor Drowning Detection Device](https://doi.org/10.1109/jsen.2024.3518436) | IEEE Sensors Journal 2025 |
| [AI-Driven AquaSense with Adaptive Learning](https://doi.org/10.1002/ett.70081) | Emerging Telecommunications Technologies 2025 |
| [Distributed Acoustic Sensing for Ocean Applications](https://doi.org/10.58046/5J60-FJ89) | Ocean Applications 2025 |


3. **Integrated Multi-Modal Approaches** (32 papers)
   - AI-IoT integration
   - Multi-sensor data fusion
   - Drone-based surveillance

| Paper | Published in |
|-------|--------------|
| [AI & IoT Integration for Beach Safety](https://doi.org/10.1109/MVT.2017.2753540) | IEEE Vehicular Technology Magazine 2017 |
| [Optimal Sensor Placement for Artificial Swimmers](https://doi.org/10.1017/jfm.2019.940) | Journal of Fluid Mechanics 2019 |
| [Sharkeye: Real-Time Shark Alert System](https://doi.org/10.3390/DRONES4020018) | Drones 2020 |
| [SafeSwim: Overhead Vision System](https://doi.org/10.1109/ARGENCON49523.2020.9505478) | IEEE ARGENCON 2020 |
| [Automated Pool Monitoring with Transfer Learning](https://doi.org/10.3390/electronics9122082) | Electronics 2020 |
| [Multi-Sensor Data Fusion Architectures](https://doi.org/10.3390/s21217007) | Sensors 2021 |
| [Ensemble ML for Water Quality Prediction](https://doi.org/10.1016/j.scitotenv.2020.142760) | Science of the Total Environment 2021 |
| [SOSeas: Neural Network Risk Assessment](https://doi.org/10.1080/1755876X.2021.1999107) | Journal of Operational Oceanography 2021 |
| [UAV-Assisted B5G/6G Mobile Edge Computing](https://doi.org/10.3390/drones6070177) | Drones 2022 |
| [Framework for Swimming Analytics with Wearables](https://doi.org/10.3390/s21155162) | Sensors 2021 |
| [AI-Driven Drowned-Detection for Coastal Rescue](https://doi.org/10.1007/s41324-023-00549-7) | Spatial Information Research 2023 |
| [BeWastMan: Autonomous Beach Waste Management](https://doi.org/10.1109/ACCESS.2023.3317689) | IEEE Access 2023 |
| [Real-Time Multi-Object Tracking with Sensor Fusion](https://doi.org/10.3390/pr11020501) | Processes 2023 |
| [Multi-Sensor Navigation for Blind & Visually Impaired](https://doi.org/10.3390/s23125411) | Sensors 2023 |
| [Cloud Computing & AI for Swimmer Technique Enhancement](https://doi.org/10.1007/s11036-023-02167-x) | Mobile Networks & Applications 2023 |
| [Robust IoT System for Smart Beaches](https://doi.org/10.1016/j.iot.2024.101295) | Internet of Things 2024 |
| [AI-Powered Pool Monitoring with IoT](https://doi.org/10.1016/j.heliyon.2024.e35484) | Heliyon 2024 |
| [5G & Drone Integration for Coastal Litter](https://doi.org/10.3390/drones8120750) | Drones 2024 |
| [Swimmer Alert System with IoT & Wi-Fi](https://doi.org/10.55524/ijircst.2024.12.4.8) | IJIRCST 2024 |
| [Advanced Sensor-Driven Drowning Prevention](https://doi.org/10.1109/ICICNIS64247.2024.10823289) | ICICNIS 2024 |
| [Drone Network for Distressed Person Localization](https://doi.org/10.3390/drones8090465) | Drones 2024 |
| [UAV Laser Scanning for Beach Monitoring](https://doi.org/10.1109/ROBOT61475.2024.10797412) | ROBOT 2024 |
| [Machine Learning for Rip Current Prediction](https://doi.org/10.1016/j.rineng.2023.101704) | Results in Engineering 2024 |
| [Novel Deep Learning for Tide Detection](https://doi.org/10.12912/27197050/200492) | Ecological Engineering 2025 |
| [Hybrid AI-Driven Wearable Sensors](https://doi.org/10.1002/ett.70081) | Emerging Telecommunications Technologies 2025 |


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
