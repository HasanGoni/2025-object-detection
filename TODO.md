# TODO and Git Workflow Guide

## Git Workflow for Solo Development

When working alone or with a single alternate account, here's the recommended Git workflow:

### Branch Strategy

1. **Main Branch (`main`)**: 
   - Always keep this branch stable and deployable
   - Never commit directly to main

2. **Development Branch (`dev`)**: 
   - Primary development branch
   - Merge to main when features are complete and tested

3. **Feature Branches**: 
   - Create for each new feature/component
   - Name format: `feature/brief-description`
   - Example: `feature/yolo-implementation`

4. **Bug Fix Branches**:
   - Create for bug fixes
   - Name format: `fix/brief-description`
   - Example: `fix/iou-calculation`

### Workflow Steps

1. **Start new work**:
   ```bash
   git checkout dev
   git pull
   git checkout -b feature/new-feature
   # Work on your feature...
   ```

2. **Commit changes regularly**:
   ```bash
   git add .
   git commit -m "Descriptive message about what you did"
   ```

3. **Push to remote**:
   ```bash
   git push -u origin feature/new-feature
   ```

4. **Merge to dev when complete**:
   ```bash
   git checkout dev
   git pull
   git merge feature/new-feature
   git push origin dev
   ```

5. **Release to main**:
   ```bash
   git checkout main
   git pull
   git merge dev
   git tag -a v0.x.0 -m "Version 0.x.0"
   git push origin main
   git push origin --tags
   ```

### Commit Guidelines

1. Write clear, concise commit messages
2. Start with a verb in present tense
3. Keep first line under 50 characters
4. Include more details in the body if needed

Examples:
- "Add YOLO model implementation"
- "Fix bounding box visualization bug"
- "Improve data augmentation pipeline"

## Project Roadmap

### Phase 1: Foundation (Current)
- [x] Initialize project structure
- [x] Set up nbdev integration
- [x] Implement core utilities
- [x] Create base dataset class
- [x] Implement Faster R-CNN model

### Phase 2: Model Expansion
- [ ] Implement YOLO v5/v8 model
- [ ] Implement SSD model
- [ ] Add model benchmarking tools
- [ ] Create model ensemble capabilities

### Phase 3: Training Improvements
- [ ] Add more learning rate schedulers
- [ ] Implement mixed precision training
- [ ] Add distributed training support
- [ ] Create automatic hyperparameter tuning

### Phase 4: Dataset Expansion
- [ ] Add Pascal VOC dataset support
- [ ] Add Open Images dataset support
- [ ] Create dataset fusion tools
- [ ] Implement advanced data augmentation techniques

### Phase 5: Advanced Features
- [ ] Add visualization dashboard
- [ ] Implement model pruning
- [ ] Create model quantization tools
- [ ] Add export to ONNX/TensorRT

## Immediate Tasks

- [ ] Finish COCO dataset integration
- [ ] Add test cases for core components
- [ ] Create documentation website
- [ ] Implement model evaluation metrics
- [ ] Add example for custom dataset training

## Notes for Collaboration
When working with your alternate account:
1. Make sure to clearly divide tasks
2. Use pull requests between accounts for code review
3. Consider setting up GitHub Actions for CI/CD
4. Use GitHub Projects for task tracking