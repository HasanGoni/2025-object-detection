# Changelog

All notable changes to the `objdetect` project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial repository setup with nbdev
- Core utilities for bounding box operations and visualization
- Data module with dataset classes and augmentation pipeline
- Models module with Faster R-CNN implementation
- Learner module with training interface similar to fastai
- Example notebook for COCO dataset

## [0.0.1] - 2025-03-24

### Added
- Project initialization
- Repository structure with nbdev support
- Core functionality:
  - Bounding box utilities (conversion between formats, IoU)
  - Visualization tools for object detection
- Data handling:
  - Base ObjectDetectionDataset class
  - Data transforms for object detection
  - COCO dataset loader stub
- Models:
  - Faster R-CNN implementation
  - YOLO stub for future implementation
  - Factory function for model creation
- Training:
  - ObjectDetectionLearner class
  - Callback system (Progress, OneCycle, Checkpointing)
  - Training and evaluation functions
- Examples:
  - Object detection on COCO dataset

## How to Update This File

When making changes to the codebase, add an entry to the "Unreleased" section following this format:

### Added
- New features

### Changed
- Changes in existing functionality

### Deprecated
- Soon-to-be removed features

### Removed
- Removed features

### Fixed
- Bug fixes

### Security
- Vulnerability fixes

Before a release, rename the "Unreleased" section to the new version number and create a new empty "Unreleased" section.

## Version Naming Convention

- **MAJOR version** when making incompatible API changes
- **MINOR version** when adding functionality in a backwards compatible manner
- **PATCH version** when making backwards compatible bug fixes