---
layout: page
title: A Deep-Learning Based Decoded EEG Neurofeedback Platform Using Muse-S
description: Open-source, portable neurofeedback platform using consumer-grade EEG and deep learning for real-time brain state decoding.
img: assets/img/platform.png
importance: 1
category: machine learning research
---

## Project Overview

This project develops an **open-source, deep learning-driven decoded EEG neurofeedback platform** that transforms expensive, immobile fMRI-based neurofeedback into an accessible, portable solution using consumer-grade Muse-S headsets. The platform enables real-time brain state decoding and feedback delivery, making neurofeedback therapy more practical for clinical applications, especially for children and patients with movement difficulties.

## Motivation & Impact

<div class="row mt-3">
    <div class="col-md-6">
        <div class="card h-100 border-danger">
            <div class="card-body">
                <h5 class="card-title text-danger"><i class="fas fa-times-circle"></i> Traditional fMRI Limitations</h5>
                <ul class="small">
                    <li>$500-700 per hour cost</li>
                    <li>Requires 3-10 sessions across days</li>
                    <li>Immobile, scanner-bound</li>
                    <li>Unsuitable for frequent clinical use</li>
                </ul>
            </div>
        </div>
    </div>
    <div class="col-md-6">
        <div class="card h-100 border-success">
            <div class="card-body">
                <h5 class="card-title text-success"><i class="fas fa-check-circle"></i> Our EEG Solution</h5>
                <ul class="small">
                    <li>Negligible running costs</li>
                    <li>Portable & wireless (Muse-S)</li>
                    <li>No gel preparation needed</li>
                    <li>Real-time feedback capability</li>
                </ul>
            </div>
        </div>
    </div>
</div>

## Technical Architecture

### Platform Components

<div class="row mt-3">
    <div class="col-md-4">
        <div class="text-center">
            <i class="fas fa-brain fa-3x text-primary mb-2"></i>
            <h5>Data Acquisition</h5>
            <p class="small">Muse-S headset with 4 dry electrodes (TP9/AF7/AF8/TP10) at 256Hz sampling rate</p>
        </div>
    </div>
    <div class="col-md-4">
        <div class="text-center">
            <i class="fas fa-network-wired fa-3x text-info mb-2"></i>
            <h5>Real-time Streaming</h5>
            <p class="small">Lab Streaming Layer (LSL) for synchronized EEG data and event markers</p>
        </div>
    </div>
    <div class="col-md-4">
        <div class="text-center">
            <i class="fas fa-robot fa-3x text-success mb-2"></i>
            <h5>Deep Learning Decoder</h5>
            <p class="small">EEGNet CNN architecture for real-time brain state classification</p>
        </div>
    </div>
</div>

### Dual-Branch System

<div class="row mt-4">
    <div class="col-md-6">
        <h5><i class="fas fa-stream"></i> Online Branch</h5>
        <p class="small"><strong>Real-time neurofeedback delivery:</strong></p>
        <ul class="small">
            <li>Live EEG streaming via LSL</li>
            <li>4-second sliding window analysis</li>
            <li>Real-time decoder predictions</li>
            <li>Visual feedback via PsychoPy UI</li>
            <li>6s induction → 2s fixation → 2s feedback cycle</li>
        </ul>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-database"></i> Offline Branch</h5>
        <p class="small"><strong>Decoder training pipeline:</strong></p>
        <ul class="small">
            <li>Data collection & quality control</li>
            <li>Event segmentation & labeling</li>
            <li>EEGNet model training</li>
            <li>Cross-session validation</li>
            <li>Model freezing for online deployment</li>
        </ul>
    </div>
</div>

## Model Performance

<div class="alert alert-success mt-3" role="alert">
    <h5 class="alert-heading text-dark"><i class="fas fa-chart-line"></i> Validation Results</h5>
    <div class="row">
        <div class="col-md-3 text-center">
            <h3 class="mb-0 text-dark">0.904</h3>
            <small class="text-dark">AUC Score</small>
        </div>
        <div class="col-md-3 text-center">
            <h3 class="mb-0 text-dark">84.8%</h3>
            <small class="text-dark">Accuracy</small>
        </div>
        <div class="col-md-3 text-center">
            <h3 class="mb-0 text-dark">0.861</h3>
            <small class="text-dark">F1-Score</small>
        </div>
        <div class="col-md-3 text-center">
            <h3 class="mb-0 text-dark">94.6%</h3>
            <small class="text-dark">Recall</small>
        </div>
    </div>
</div>

### EEGNet Architecture Details

The decoder employs a compact convolutional neural network specifically designed for EEG-based BCIs:

<div class="row">
    <div class="col-md-12">
        <ul class="small">
            <li><strong>Input:</strong> 2 channels (TP9, TP10) × 1024 time points (4 seconds at 256Hz)</li>
            <li><strong>Block 1:</strong> Temporal convolution (8 filters, 1×64 kernel) for frequency-specific features</li>
            <li><strong>Block 2:</strong> Depthwise spatial convolution (16 filters, 2×1 kernel) with ELU activation</li>
            <li><strong>Block 3:</strong> Separable convolution (16 filters, 1×16 kernel) combining temporal-spatial info</li>
            <li><strong>Output:</strong> Binary classification (motor vs. rest state)</li>
        </ul>
    </div>
</div>

## Clinical Applications

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-child text-primary"></i> Pediatric Therapy</h5>
        <p class="small">Suitable for children with ADHD or autism who cannot tolerate gel-based EEG or fMRI scanners</p>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-wheelchair text-info"></i> Motor Rehabilitation</h5>
        <p class="small">Portable neurofeedback for stroke patients and individuals with motor disabilities</p>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-brain text-warning"></i> Cognitive Training</h5>
        <p class="small">Attention enhancement and working memory improvement through targeted neurofeedback</p>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-heartbeat text-danger"></i> Mental Health</h5>
        <p class="small">Potential applications in anxiety, phobia, and PTSD treatment protocols</p>
    </div>
</div>


## Resources

<div class="row mt-3">
    <div class="col-md-6">
        <a href="https://github.com/xinyanghe08/DecNef-EEG" class="btn btn-dark btn-block" target="_blank">
            <i class="fab fa-github"></i> Source Code
        </a>
    </div>
    <div class="col-md-6">
        <a href="/assets/pdf/decnef_poster_final.pdf" class="btn btn-success btn-block" target="_blank">
            <i class="fas fa-file-pdf"></i> Research Poster
        </a>
    </div>
</div>
## Update
I am currently working on the manuscript, and the compelte manuscript is expected to be done by the end of December 2025.
