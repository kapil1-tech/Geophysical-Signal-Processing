# Geophysical Signal Processing for Seismic Event Detection Using STA/LTA Analysis

## Project Description

This project presents a basic geophysical signal processing workflow for detecting seismic events in noisy seismic data. The implementation focuses on generating a synthetic seismic signal, applying digital filtering techniques to improve signal quality, and using the Short-Term Average / Long-Term Average (STA/LTA) method to identify potential seismic events.

Signal processing techniques are widely used in geophysics to analyze seismic recordings, remove noise, and detect events such as earthquakes, microseismic activity, and subsurface disturbances. This project demonstrates these fundamental concepts using Python.

---

## Problem Statement

Seismic recordings often contain significant background noise that can obscure important events. Manual inspection of large volumes of seismic data is time-consuming and inefficient.

The objective of this project is to develop a simple automated workflow that:

* Generates a seismic waveform containing noise and an artificial seismic event.
* Reduces noise using a bandpass filter.
* Computes the STA/LTA characteristic function.
* Detects events based on a threshold criterion.
* Visualizes each processing stage.

---

## Objectives

The primary objectives of this project are:

1. Simulate a seismic waveform for analysis.
2. Apply digital signal processing techniques to improve signal quality.
3. Implement the STA/LTA event detection algorithm.
4. Identify portions of the signal corresponding to seismic activity.
5. Visualize and interpret the results.

---

## Background

### Seismic Signals

Seismic signals are vibrations recorded by sensors known as seismometers. These signals contain information about subsurface events and geological structures. However, raw seismic data often include environmental and instrumental noise.

### Signal Processing in Geophysics

Signal processing techniques help improve data quality by:

* Removing unwanted noise.
* Enhancing useful signal components.
* Detecting significant events automatically.
* Supporting interpretation of geophysical data.

### STA/LTA Method

The STA/LTA (Short-Term Average / Long-Term Average) algorithm is a commonly used technique for automatic seismic event detection.

The algorithm compares:

* A short-term average (STA), representing recent signal energy.
* A long-term average (LTA), representing background signal energy.

The STA/LTA ratio increases significantly when a seismic event occurs. Event detection is performed when this ratio exceeds a predefined threshold.

---

## Methodology

### Step 1: Synthetic Seismic Signal Generation

A synthetic seismic signal is generated using NumPy. Random noise is added to simulate background seismic noise. An artificial seismic event is introduced at a specific time interval.

### Step 2: Bandpass Filtering

A Butterworth bandpass filter is applied to the signal.

Purpose:

* Remove low-frequency drift.
* Remove high-frequency noise.
* Preserve frequencies associated with seismic events.

### Step 3: STA/LTA Computation

The STA and LTA windows are computed using moving averages of the absolute signal amplitude.

The STA/LTA ratio is calculated as:

STA/LTA = Short-Term Average / Long-Term Average

### Step 4: Event Detection

A threshold value is selected for the STA/LTA ratio.

If:

STA/LTA > Threshold

the corresponding sample is marked as a detected seismic event.

### Step 5: Visualization

Plots are generated for:

* Raw seismic signal
* Filtered seismic signal
* STA/LTA ratio
* Detected events

---

## Project Workflow

```text
Synthetic Seismic Signal
          ↓
Bandpass Filtering
          ↓
STA/LTA Calculation
          ↓
Threshold-Based Detection
          ↓
Result Visualization
```

---

## Technologies and Libraries Used

| Library          | Purpose                 |
| ---------------- | ----------------------- |
| Python           | Programming Language    |
| NumPy            | Numerical Operations    |
| SciPy            | Signal Filtering        |
| Matplotlib       | Data Visualization      |
| Jupyter Notebook | Development Environment |

---

## Repository Structure

```text
Geophysical-Signal-Processing/
│
├── Geophysical_Signal_Processing.ipynb
├── README.md
├── requirements.txt
│
├── data/
│
└── results/
    ├── raw_signal.png
    ├── filtered_signal.png
    ├── sta_lta_ratio.png
    └── event_detection.png
```

---

## Results

The implemented workflow successfully demonstrates:

* Generation of a synthetic seismic signal.
* Noise reduction through bandpass filtering.
* Computation of the STA/LTA characteristic function.
* Automatic detection of the inserted seismic event.
* Visualization of signal behavior before and after processing.

The detected events correspond to the region where the synthetic seismic activity was introduced into the signal.

---

## Limitations

This project uses synthetic data generated for educational purposes. Therefore:

* Results may differ from real seismic recordings.
* Only a single-channel signal is analyzed.
* Detection performance depends on selected window lengths and threshold values.

---

## Future Scope

Possible future improvements include:

* Analysis of real earthquake waveform datasets.
* Adaptive threshold selection.
* Comparison with other event detection techniques.
* Frequency-domain seismic analysis.
* Integration with machine learning methods for classification.

---

## Conclusion

This project demonstrates the application of basic geophysical signal processing techniques for seismic event detection. By combining bandpass filtering and STA/LTA analysis, the workflow is able to identify seismic activity within a noisy signal. The project provides a practical introduction to signal processing methods commonly used in seismic data analysis and earthquake monitoring.

---


