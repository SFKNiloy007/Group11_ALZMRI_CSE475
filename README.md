# CSE475 Project

- **Group:** 11
- **Dataset:** Alzheimer MRI (`ALZMRI`)
- **Track:** Track 2 — Graph Convolutional Network (image → graph)

## Repository layout

- `report/task1/`, `report/task2/`, `report/task3/`: short task reports (one due at the end of each task)
- `Code/Task 1/`, `Code/Task 2/`, `Code/Task 3/`: task notebooks and code
- `related_work/`: related work table and source papers in `papers/`
- `models/`: trained model checkpoints and label map

## Results

Task 1 (completed): age-confound control (75.9 vs 76.8 yrs, p = 0.44) and the tabular reference bar — age + nWBV at 0.742 AUC

Task 2 (completed): 31 image models on identical subject-wise 5-fold splits
Proposed DenseNet201 + GCN + Attention: pooled AUC 0.735 (CI 0.659–0.801), +0.106 over the plain backbone (p = 0.009), p = 0.042 vs GCN-only, n.s. vs attention-only
Baselines: leading CNNs 0.733–0.736 pooled AUC (statistically tied), best superpixel GNN 0.702 (clearly below)
Honest headline: no image model beats the 0.742 tabular reference → motivates Task 3
Error analysis: 34% of CDR 0.5 missed vs 10% of CDR 1+ (p = 0.014); 34 subjects wrong under every baseline

Task 3: TBA



