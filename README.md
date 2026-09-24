# OrbitVision — Onboard Satellite Cloud Filtering

A lightweight deep-learning project exploring whether satellite images are useful enough to transmit to Earth. The intended model flags mostly cloud-obstructed imagery to help study the tradeoff between retaining useful images and reducing downlink volume.

**Status: planned / repository setup.** No model has been trained or benchmarked. This is a research prototype concept, not a flight-deployed system.

## Stack
Python · PyTorch · MobileNet · FastAPI · React

## Planned pipeline
Satellite image → preprocessing → lightweight CNN → cloud-obstruction score → threshold decision: SEND or DISCARD.

The initial scope is binary useful/cloud-obstructed classification. A classifier's probability is not a measured cloud coverage percentage. Any future coverage estimate will require suitable labels and separate validation.

## MVP roadmap
- [ ] Choose a public satellite imagery dataset and document its license
- [ ] Define useful/cloud-obstructed labels and decision thresholds
- [ ] Create train, validation, and held-out test splits that limit scene or geographic leakage
- [ ] Fine-tune a lightweight MobileNet model with PyTorch
- [ ] Evaluate precision, recall, F1, and confusion matrices
- [ ] Measure saved model size and CPU inference latency
- [ ] Analyze useful images incorrectly discarded and cloudy images retained
- [ ] Compare baseline and optimized inference, including quantization if supported
- [ ] Add a FastAPI inference endpoint and React upload interface
- [ ] Document reproducible training, evaluation, and benchmarking commands

## Evaluation and edge constraints
Report the dataset, split strategy, label definitions, and per-class metrics. Select the decision threshold on validation data and report final results on held-out test data.

Benchmark on named hardware with input size, batch size, CPU thread count, warm-up procedure, and repeated-run median and p95 latency. Report model size and any accuracy changes after optimization. Desktop CPU measurements do not establish flight-hardware performance or power consumption.

## Results
Pending actual experiments. No accuracy, latency, memory, or downlink savings claims are made yet.

## Engineering focus
Computer vision, transfer learning, model evaluation, edge ML constraints, and inference optimization.
