[![NSF-1948997](https://img.shields.io/badge/NSF-2409885-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=2409885) [![NSF-2409886](https://img.shields.io/badge/NSF-2409886-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=2409886) [![NSF-2409887](https://img.shields.io/badge/NSF-2409887-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=2409887)

# Measuring Tree Structure from a Lidar Point Cloud

This repository holds a hands-on activity that introduces two structural measurements of a tree. Canopy height describes how tall a tree stands from the ground to its top. Crown width describes how far the tree's branches spread. Both can be measured directly from a lidar point cloud, without going into the field.

Students work in CloudCompare, a free and open source point cloud viewer used in surveying, forestry and the geosciences. Unlike a browser-based viewer, CloudCompare runs on the student's own machine and gives direct access to the full point cloud rather than a rendered preview. Students use the point picking tool to select points and read the distance between them, repeat each measurement five times to see how the value shifts with each pick, and then average the results.

The activity uses two versions of the same dataset. The standard point cloud stores each Z value as elevation above sea level, so a tree on a hill carries the hill's height inside its Z value. The normalized point cloud has the terrain removed, so the ground sits flat at zero and Z becomes canopy height directly. Comparing the two shows students what normalization does and its impact in measuring trees. 

**Learning goal:** By the end of this activity, students will be able to measure canopy height and crown width from a lidar point cloud in CloudCompare and explain why multiple measurements of the same feature can vary. 

**Objectives:**

* Define canopy height and crown width.
* Identify the CloudCompare tools used to measure canopy height and crown width.
* Measure canopy height on both the standard and normalized clouds, and crown width along two perpendicular diameters.
* Compare five repeat measurements per tree and account for the spread.
* Complete the measurement tables and report and justify an average canopy height and crown width for each tree.

## Audience

This activity is designed for **freshman and sophomore students**, and assumes no prior experience with CloudCompare. It fits courses in **forest ecology, remote sensing, GIS, natural resource management and environmental science**. It follows the OpenForest4D lidar introduction activities - [Activities 1-2: Lidar Point Clouds and Gridded Data for Forest Analysis](https://github.com/OpenForest4D/lidar_basic_concepts_and_exercises), but can also be assigned on its own.

## Activity

**Understanding Canopy Height and Crown Width of a Tree Using CloudCompare**

Students read a short introduction to normalized point clouds, canopy height models and crown width, then install CloudCompare and load both point clouds. They select five trees and measure canopy height on each, first on the standard cloud using two-point distance mode and then on the normalized cloud using single-point mode. They then switch to a top-down view and measure crown width along two perpendicular diameters. Each measurement is repeated five times and averaged in the tables provided. Questions at the end ask students to interpret the spread in their values, explain crown asymmetry, and judge which cloud is better suited to mapping canopy height across a full landscape.

The activity document is provided in two formats:

* **`.docx`** — fully editable, so instructors can adapt the readings, steps and tables to their own course.
* **`.pdf`** — a fixed, print-ready version for students who just need to follow along.

## Software

CloudCompare is free and runs on Windows, macOS and Linux. Download the latest stable installer from the [official release page](https://www.cloudcompare.org/release/). Use the installer rather than the zip archive. Installation needs admin rights and may require a restart.

## Getting Started

All instructions are provided in the activity document.

1. Download both `.laz` files from the `data` folder.
2. Install CloudCompare from [www.cloudcompare.org](https://www.cloudcompare.org/).
3. Open the document (`.docx` or `.pdf`) in the `activities` folder and follow it from Step 1 of the Lab Activity.

## Data

The activity expects two `.laz` files, retrievable from this repository under the `data/` folder.

The `data/` folder contains two files:

* A lidar point cloud in `.laz` format, with Z as elevation above sea level (segmented_trees.laz).
* A height normalized version of the same point cloud, with ground at Z equal to zero (normalized_segmented_trees.laz).

## Repository Structure

```
lidar_applied_tree_measurements/
├── activities/
│   ├── activity_3_Computing_Canopy_Height_and_Crown_Width_using_CloudCompare.docx  # Editable activity document
│   └── activity_3_Computing_Canopy_Height_and_Crown_Width_using_CloudCompare.pdf   # Print-ready activity document
├── data/
│   ├── segmented_trees.laz                         # Raw lidar point cloud
│   └── normalized_segmented_trees.laz              # Height normalized point cloud
├── LICENSE
└── README.md
```

## For Instructors

> **Part of a two-repo lidar activity sequence.** This is **activity
> 3** in the sequence. Intial activities 1-2 available in a seperate repository.
> - [Activities 1-2: Lidar Point Clouds and Gridded Data for Forest Analysis](https://github.com/OpenForest4D/lidar_basic_concepts_and_exercises)

The `.docx` activity sheet is fully editable, allowing you to adapt it to your course needs. For an answer key to the in-activity questions, please contact [OpenForest4D](https://openforest4d.org/contact/).

## Acknowledgments

* This material is developed as part of the OpenForest4D project funded by NSF awards 2409885, 2409886 & 2409887.
* Lidar data: U.S. Geological Survey (2021). AZ USFS 3DEP Processing 2019. Distributed by OpenTopography. https://portal.opentopography.org/usgsDataset?dsid=AZ_USFS_3DEP_Processing_2019
* [CloudCompare](https://www.cloudcompare.org/) and other open source tools.
