# Kolam Type Classifier — SIH 2025 (Team HeritEdge)

My ML component from our Smart India Hackathon 2025 project (PS 25107 — identify design principles behind Kolam designs and recreate them). Kept private as a personal archive.

- **Task:** classify kolam images into 6 traditional types
- **Data:** ~1,443 images (1,012 train / 213 val / 218 test), team-collected; corrupt files detected and removed via PIL `verify()`
- **Model:** MobileNetV2 (ImageNet weights, frozen) → GlobalAveragePooling → Dense(128, relu) → Dropout(0.3) → softmax(6)
- **Augmentation:** rotation, shifts, shear, zoom, horizontal flip — training set only
- **Result:** **94.95% test accuracy** after 10 epochs
- Includes an OpenCV `predict_kolam()` inference helper that labels an input image

Note: the team's Django analysis/recreation app lives in a teammate's repository; this classifier was my classification component of the proposed pipeline.

**Author:** Pragun Aggarwal — B.Tech CSE, Thapar Institute
