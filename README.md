# CancerVision

An educational deep-learning project for classifying skin lesion image categories using transfer learning.

**Status: planning / initial repository setup.** No dataset has been selected, no model has been trained, and no performance results are available yet.

**Educational and research use only. Not a clinical diagnostic tool.**

## Planned stack
Python, PyTorch, ResNet18, FastAPI, React.

## MVP roadmap
- [ ] Select a public labeled research dataset and document its license
- [ ] Create reproducible training, validation, and held-out test splits
- [ ] Prevent patient or lesion overlap across splits where identifiers are available
- [ ] Implement preprocessing and training-only augmentation
- [ ] Fine-tune ResNet18 and address class imbalance
- [ ] Evaluate precision, recall, macro F1, and confusion matrices
- [ ] Analyze per-class errors and limitations
- [ ] Save model weights and training configuration
- [ ] Build a FastAPI prediction endpoint
- [ ] Build a React image upload interface
- [ ] Add reproducible setup and inference instructions

## Evaluation plan
Tune using the training and validation sets; reserve the test set for final evaluation. Report the dataset version, split method, class counts, and measured results. Model probabilities should not be presented as clinical certainty.

## Results
Pending actual training and evaluation. No accuracy or F1 claims are made at this stage.
