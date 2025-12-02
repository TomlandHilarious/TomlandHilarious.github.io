---
layout: page
title: Hands-Free Dino Jump
description: Play the dinosaur game using eye-blinks detected from EEG signals, without touching the keyboard.

img: assets/img/dino_jump.png
importance: 3
category: side projects
---

## The Challenge: Playing Games Hands-Free

This project is my final course project for COGS 189: Brain Computer Interfaces at UCSD.

What if you could play a game without touching a keyboard? What if people with motor disabilities could enjoy games through their brain signals? This project explores using **eye-blinks detected from EEG signals** to control the classic Dinosaur Game—no hands required.

## Demo

Watch the system in action:

<div class="row mt-3">
    <div class="col-md-8 mx-auto">
        <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/qMAVhjj_hBw" allowfullscreen></iframe>
        </div>
    </div>
</div>

## Motivation

We were driven by three key questions:

<div class="row mt-3">
    <div class="col-md-4">
        <div class="card h-100 border-primary">
            <div class="card-body">
                <h6 class="card-title text-primary"><i class="fas fa-question-circle"></i> BCI vs. Keyboard</h6>
                <p class="small mb-0">Is an open BCI easier or harder to use than a keyboard for gaming?</p>
            </div>
        </div>
    </div>
    <div class="col-md-4">
        <div class="card h-100 border-success">
            <div class="card-body">
                <h6 class="card-title text-success"><i class="fas fa-wheelchair"></i> Accessibility</h6>
                <p class="small mb-0">How can people with motor disabilities or keyboard difficulties play games?</p>
            </div>
        </div>
    </div>
    <div class="col-md-4">
        <div class="card h-100 border-info">
            <div class="card-body">
                <h6 class="card-title text-info"><i class="fas fa-eye"></i> Eyeblink Signals</h6>
                <p class="small mb-0">How effective are eyeblinks (vs. actual brain activity) in an online BCI?</p>
            </div>
        </div>
    </div>
</div>

## Methodology

### Data Collection

We recorded EEG signals from **4 participants** using an **OpenBCI Cyton** device, focusing on eyeblink detection:

- **Electrodes:** FP1 and FP2 (closest to the eyes, best for eyeblink signals)
- **Trials per participant:** 5 trials × 60 seconds each
- **Trial structure:**
  - First 30 seconds: Single blink every 5 seconds
  - Last 30 seconds: Double blink every 5 seconds
- **Total data:** 20 trials across all participants

### Signal Processing Pipeline

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-wave-square"></i> Offline Processing</h5>
        <ol class="small">
            <li><strong>Data extraction</strong> - Extract FP1 & FP2 from CSV files</li>
            <li><strong>Normalization</strong> - Flip inverted signals, normalize drift</li>
            <li><strong>Filtering</strong> - Apply high-pass and low-pass filters</li>
            <li><strong>Epoching</strong> - Divide into 5.2-second windows</li>
            <li><strong>Peak detection</strong> - Mark peaks and measure amplitudes</li>
        </ol>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-brain"></i> Key Observations</h5>
        <ul class="small">
            <li>Eyeblinks show distinctive voltage drops</li>
            <li>Double blinks have stronger first peak</li>
            <li>Second blink has lower amplitude</li>
            <li>Clear 5-second periodicity in data</li>
        </ul>
    </div>
</div>

### Simple Voltage Thresholding (SVT)

We distinguished single vs. double blinks using two features:

<div class="alert alert-info mt-3" role="alert">
    <h6 class="alert-heading text-dark"><i class="fas fa-chart-bar"></i> SVT Features</h6>
    <p class="small mb-0 text-dark"><strong class="text-dark">1. Peak Magnitude:</strong> Double blinks have stronger peaks than single blinks</p>
    <p class="small mb-0 text-dark"><strong class="text-dark">2. Peak Interval:</strong> Double blinks show a high peak followed by another peak with slightly lower amplitude</p>
    <p class="small mb-0 text-dark"><strong class="text-dark">Threshold:</strong> Calculated by averaging peak magnitudes for each participant</p>
</div>

## How It Works: Online BCI System

<div class="row mt-3">
    <div class="col-md-12">
        <div class="card">
            <div class="card-body">
                <h6 class="card-title"><i class="fas fa-cogs"></i> Real-Time Pipeline</h6>
                <ol class="small">
                    <li><strong>Stream data</strong> - Python LSL package receives online EEG data</li>
                    <li><strong>Classify</strong> - Apply SVT model to categorize signals as double-blinks or not</li>
                    <li><strong>Control</strong> - Pynput simulates spacebar press/release</li>
                    <li><strong>Jump!</strong> - Dinosaur jumps when spacebar is released</li>
                </ol>
            </div>
        </div>
    </div>
</div>

## Optimal Parameters

After extensive optimization, we determined the best settings for real-time classification:

<div class="alert alert-success mt-3" role="alert">
    <h6 class="alert-heading text-dark"><i class="fas fa-star"></i> Optimal Configuration</h6>
    <p class="small mb-0 text-dark"><strong class="text-dark">Sampling window:</strong> 375 data points</p>
    <p class="small mb-0 text-dark"><strong class="text-dark">Peak-to-peak interval:</strong> 150 data points</p>
    <p class="small mb-0 text-dark"><strong class="text-dark">Result:</strong> Rapid processing + accurate classification</p>
</div>

## What We Learned

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-graduation-cap"></i> Technical Insights</h5>
        <ul class="small">
            <li>BCI data processing pipelines (OpenBCI Cyton)</li>
            <li>Signal processing techniques (filtering, normalization)</li>
            <li>Simple Voltage Thresholding algorithm</li>
            <li>Real-time EEG classification challenges</li>
        </ul>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-exclamation-triangle"></i> Limitations & Challenges</h5>
        <ul class="small">
            <li><strong>Small sample:</strong> Only 4 participants limited generalization</li>
            <li><strong>Manual parameters:</strong> Time constraints required hand-tuned thresholds</li>
            <li><strong>Latency:</strong> Delay between blink and game response</li>
            <li><strong>Incomplete implementation:</strong> Only jump action; duck action not implemented</li>
        </ul>
    </div>
</div>

## Key Takeaway
 While detecting the second eyeblink remains difficult, the system demonstrates the feasibility of using consumer-grade EEG and eyeblink signals for real-time game control. This opens possibilities for accessible gaming and interaction for people with motor disabilities.


## Repository

**[View the code on GitHub](https://github.com/TomlandHilarious/COGS-189-Dinosaur-Game-with-Eyeblink)**
