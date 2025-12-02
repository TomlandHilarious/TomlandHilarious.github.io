---
layout: page
title: Understanding Fears and Confidence amongst Non-majors in Introductory CS Courses
description: Understanding how non-majors experience introductory CS courses and the impact of course design on confidence.
img: assets/img/fear_coding.jpg
importance: 3
category: human-centered research
---

## The Challenge: Why Do Non-Majors Fear CS?

Computer Science is increasingly becoming a required or recommended course for non-majors across universities. However, many students entering these courses carry significant fears and anxieties about their ability to succeed. Understanding these fears and how different course designs impact student confidence is crucial for improving the learning experience.

This study investigates the fears of non-major students in introductory CS courses and compares how their confidence levels change in two different course types: **CS0** (designed specifically for non-majors) and **CS1** (traditional introductory CS course).

## Research Questions

We aimed to answer three key questions:

<div class="row mt-3">
    <div class="col-md-4">
        <div class="card h-100 border-primary">
            <div class="card-body">
                <h5 class="card-title text-primary"><i class="fas fa-question-circle"></i> RQ1</h5>
                <p class="small"><strong>What are the fears of non-majors taking an introductory CS course?</strong></p>
            </div>
        </div>
    </div>
    <div class="col-md-4">
        <div class="card h-100 border-info">
            <div class="card-body">
                <h5 class="card-title text-info"><i class="fas fa-question-circle"></i> RQ2</h5>
                <p class="small"><strong>How do confidence levels differ between CS0 and CS1 students?</strong></p>
            </div>
        </div>
    </div>
    <div class="col-md-4">
        <div class="card h-100 border-success">
            <div class="card-body">
                <h5 class="card-title text-success"><i class="fas fa-question-circle"></i> RQ3</h5>
                <p class="small"><strong>Is there a connection between initial fears and confidence change?</strong></p>
            </div>
        </div>
    </div>
</div>

## Methodology

### Study Design
- **Participants:** 626 non-major students (124 in CS0, 502 in CS1)
- **Data Collection:** Pre- and post-course surveys via Google Forms
- **Instructor:** Same instructor taught both courses for consistency

### Analysis Approach

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-code"></i> Qualitative Analysis</h5>
        <p class="small"><strong>For identifying fears:</strong></p>
        <ul class="small">
            <li>Open coding of student responses</li>
            <li>Two independent coders with consensus resolution</li>
            <li>Inter-rater reliability: 0.889 (near perfect agreement)</li>
            <li>Identified 9 distinct fear categories</li>
        </ul>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-chart-bar"></i> Quantitative Analysis</h5>
        <p class="small"><strong>For confidence comparison:</strong></p>
        <ul class="small">
            <li>Mann-Whitney U tests on confidence levels</li>
            <li>Bonferroni correction for multiple comparisons</li>
            <li>Analysis of confidence change by fear category</li>
        </ul>
    </div>
</div>

## Key Findings

### 🎯 Finding 1: Nine Categories of Fear

Students expressed fears that fell into nine distinct categories:

<div class="row mt-3">
    <div class="col-md-6">
        <div class="alert alert-warning" role="alert">
            <h6 class="alert-heading text-dark"><i class="fas fa-code text-danger"></i> Coding</h6>
            <small class="text-dark">Fear of programming itself; concerns about writing code</small>
        </div>
        <div class="alert alert-info" role="alert">
            <h6 class="alert-heading text-dark"><i class="fas fa-brain text-primary"></i> Comprehension</h6>
            <small class="text-dark">Worry about understanding course material</small>
        </div>
        <div class="alert alert-danger" role="alert">
            <h6 class="alert-heading text-dark"><i class="fas fa-users text-danger"></i> Being Left Behind</h6>
            <small class="text-dark">Fear of performing worse than peers</small>
        </div>
    </div>
    <div class="col-md-6">
        <div class="alert alert-secondary" role="alert">
            <h6 class="alert-heading text-dark"><i class="fas fa-graduation-cap"></i> Preparation</h6>
            <small class="text-dark">Feeling unprepared or lacking background knowledge</small>
        </div>
        <div class="alert alert-success" role="alert">
            <h6 class="alert-heading text-dark"><i class="fas fa-flask"></i> STEM Difficulty</h6>
            <small class="text-dark">Perceiving STEM as inherently difficult</small>
        </div>
        <div class="alert alert-light border" role="alert">
            <h6 class="alert-heading text-dark"><i class="fas fa-plus-circle"></i> + 4 More</h6>
            <small class="text-dark">Workload, grading, help-seeking, loss of interest</small>
        </div>
    </div>
</div>

### 📈 Finding 2: CS0 Students Show Greater Confidence Gains

**Key Result:** CS0 students experienced a **statistically significant increase in confidence** compared to CS1 students.

<div class="row mt-3">
    <div class="col-md-6">
        <div class="card h-100 border-success">
            <div class="card-body">
                <h5 class="card-title text-success"><i class="fas fa-arrow-up"></i> CS0 (Non-Major Focused)</h5>
                <p class="small">Designed specifically for non-majors using Snap! (visual programming)</p>
                <p class="mb-0"><strong>Result:</strong> Larger confidence gains</p>
            </div>
        </div>
    </div>
    <div class="col-md-6">
        <div class="card h-100 border-secondary">
            <div class="card-body">
                <h5 class="card-title text-secondary"><i class="fas fa-arrow-right"></i> CS1 (Traditional)</h5>
                <p class="small">Traditional intro course using Python, designed for CS majors</p>
                <p class="mb-0"><strong>Result:</strong> Smaller confidence gains</p>
            </div>
        </div>
    </div>
</div>

**Important:** Both groups started with similar initial confidence levels, so the difference is due to course design, not student selection.

### 🔗 Finding 3: Specific Fears Predict Confidence Growth

Students with certain fears showed the **highest confidence increases**:

<div class="alert alert-success mt-3" role="alert">
    <h5 class="alert-heading text-dark"><i class="fas fa-trophy"></i> Top Confidence Gainers</h5>
    <div class="row">
        <div class="col-md-4 text-center">
            <h6 class="text-dark">Coding Fears</h6>
            <p class="small text-dark">~20% of students; experienced highest gains</p>
        </div>
        <div class="col-md-4 text-center">
            <h6 class="text-dark">Preparation Concerns</h6>
            <p class="small text-dark">Students underestimated their readiness</p>
        </div>
        <div class="col-md-4 text-center">
            <h6 class="text-dark">Being Left Behind</h6>
            <p class="small text-dark">Fears about peer comparison resolved</p>
        </div>
    </div>
</div>

**Interpretation:** Students with these fears likely had low initial self-efficacy beliefs, and the course experience directly addressed these concerns, leading to substantial confidence growth.

## Implications for CS Education

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-lightbulb"></i> For Course Designers</h5>
        <ul class="small">
            <li>Course design matters significantly for non-majors</li>
            <li>CS0-style courses (creative, visual) boost confidence more</li>
            <li>Addressing self-efficacy beliefs is crucial</li>
            <li>Consider non-major-specific pedagogy</li>
        </ul>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-users"></i> For Instructors</h5>
        <ul class="small">
            <li>Acknowledge and validate student fears</li>
            <li>Create a supportive, non-judgmental environment</li>
            <li>Emphasize that fears are common and addressable</li>
            <li>Celebrate early wins to build confidence</li>
        </ul>
    </div>
</div>

## Bottom Line

**Course design significantly impacts non-major student confidence in CS.** A course specifically designed for non-majors—emphasizing creativity, exploration, and broader CS concepts—leads to greater confidence gains than a traditional CS1 course. Moreover, students who enter with the most fears (about coding, preparation, or being left behind) often experience the greatest confidence growth, suggesting that well-designed courses can directly address these concerns.

This research highlights the importance of **intentional course design for non-majors** and demonstrates that with the right pedagogical approach, we can transform student fears into confidence and engagement with computer science.

## Publication

This work was published in the **Proceedings of the 54th ACM Technical Symposium on Computer Science Education (SIGCSE 2023)**:

*Li, R., Hogan, E., & Soosai Raj, A. G. (2023). CS0 vs. CS1: Understanding Fears and Confidence amongst Non-majors in Introductory CS Courses.*

<div class="row mt-3">
    <div class="col-md-6">
        <a href="assets/pdf/cs0cs1.pdf" class="btn btn-info btn-block" target="_blank">
            <i class="fas fa-file-pdf"></i> Read the Paper
        </a>
    </div>
    <div class="col-md-6">
        <a href="https://dl.acm.org/doi/pdf/10.1145/3545945.3569865" class="btn btn-primary btn-block" target="_blank">
            <i class="fas fa-external-link-alt"></i> ACM Digital Library
        </a>
    </div>
</div>
