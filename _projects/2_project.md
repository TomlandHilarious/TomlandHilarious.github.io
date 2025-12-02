---
layout: page
title: Challenges and Approaches to Teaching CS1 in Prison
description: Designing and teaching an introductory computing course for incarcerated students.
img: assets/img/Prison_Education.jpg
importance: 2
category: human-centered research
---

## The Opportunity: Computing Education for Incarcerated Students

Bringing computing education to incarcerated and formerly incarcerated individuals is a powerful way to improve equitable access to computing careers and bring diverse perspectives into the field. However, teaching CS in a prison environment presents unique challenges that differ significantly from traditional college classrooms.

This report describes our experience designing and teaching an introductory CS1 course to **26 incarcerated students** at a U.S. prison in Fall 2022. We discovered that while environmental barriers were substantial, the student population had remarkable strengths that could be leveraged for effective learning.

## The Challenge: Environmental Barriers

<div class="row mt-3">
    <div class="col-md-6">
        <div class="card h-100 border-danger">
            <div class="card-body">
                <h5 class="card-title text-danger"><i class="fas fa-exclamation-triangle"></i> Major Obstacles</h5>
                <ul class="small mb-0">
                    <li><strong>No code interpreter access</strong> - Students couldn't run code to test it</li>
                    <li><strong>Limited resources</strong> - No tutors, TAs, or outside materials</li>
                    <li><strong>Restricted access</strong> - Limited study space (6-8 hours/week)</li>
                    <li><strong>No debugging opportunity</strong> - Critical learning experience lost</li>
                    <li><strong>Limited communication</strong> - No reliable contact outside class</li>
                </ul>
            </div>
        </div>
    </div>
    <div class="col-md-6">
        <div class="card h-100 border-success">
            <div class="card-body">
                <h5 class="card-title text-success"><i class="fas fa-star"></i> Unique Strengths</h5>
                <ul class="small mb-0">
                    <li><strong>Maturity & self-sufficiency</strong> - Adult learners with life experience</li>
                    <li><strong>Strong community</strong> - Deep sense of collective effort</li>
                    <li><strong>Independent learning skills</strong> - Experience with correspondence courses</li>
                    <li><strong>High engagement</strong> - Fully invested in learning</li>
                    <li><strong>Peer support</strong> - Natural mentoring relationships</li>
                </ul>
            </div>
        </div>
    </div>
</div>

## Methodology: Design Experiment Approach

We adopted a **design experiment methodology** to navigate the many unknowns of teaching CS in prison. This approach allowed us to:

- **Gather continuous feedback** through weekly reflection assignments (mix of Likert-scale and open-ended questions)
- **Adapt course design** based on student experiences and pressing issues
- **Capture the richness** of the classroom environment rather than oversimplifying
- **Learn from students' natural patterns** of behavior and collaboration

### Data Analysis

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-comments"></i> Qualitative Coding</h5>
        <ul class="small">
            <li>Open coding of reflection responses</li>
            <li>Two independent coders with consensus</li>
            <li>Inter-rater reliability: 0.837-0.849</li>
            <li>Focus: collaboration policies, code examples</li>
        </ul>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-graduation-cap"></i> Learning Assessment</h5>
        <ul class="small">
            <li>10 "benchmarking" questions on final exam</li>
            <li>Core CS1 skills: code tracing, explaining, writing</li>
            <li>Measured student learning outcomes</li>
        </ul>
    </div>
</div>

## Key Lessons Learned

### 1. 🤝 Leverage the Strong Student Community

The most powerful asset was the **deep sense of collective effort** among students. Despite environmental constraints:

<div class="alert alert-info mt-2" role="alert">
    <p class="small mb-0 text-dark"><strong class="text-dark">What we observed:</strong> Students spoke in terms of "we" rather than "I". They formed study groups where higher-performing students helped struggling students trace code on whiteboards and draw memory diagrams together. During Peer Instruction activities, strong students would move to sit with struggling peers.</p>
</div>

**Takeaway:** Design courses that explicitly foster and celebrate community learning.

### 2. 💡 Make Students a Resource for Each Other

Without access to outside tutors or resources, students became each other's primary learning support:

<div class="alert alert-success mt-2" role="alert">
    <p class="small mb-0 text-dark"><strong class="text-dark">Result:</strong> No student was left behind. Positive relationships formed between lower- and higher-performing students. However, this dependency made independent coding on exams challenging—students relied heavily on peer collaboration.</p>
</div>

**Takeaway:** Balance peer learning with opportunities for independent practice.

### 3. 🔄 Code Resubmission Policies are Critical

The absence of a code interpreter was the **single largest hurdle**:

<div class="row mt-3">
    <div class="col-md-6">
        <div class="card h-100">
            <div class="card-body">
                <h6 class="card-title">The Problem</h6>
                <p class="small mb-0">Students couldn't test code before submitting, and lost the critical learning that happens through debugging.</p>
            </div>
        </div>
    </div>
    <div class="col-md-6">
        <div class="card h-100 border-success">
            <div class="card-body">
                <h6 class="card-title text-success">Our Solution</h6>
                <p class="small mb-0">Unlimited resubmissions with instructor feedback, simulating the debugging process.</p>
            </div>
        </div>
    </div>
</div>

### 4. 📝 Mix Live Coding with Board Examples

Students had strong preferences for how code was presented:

<div class="row mt-3">
    <div class="col-md-12">
        <table class="table table-sm small">
            <thead>
                <tr>
                    <th>Method</th>
                    <th>Preference %</th>
                    <th>Student Quote</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>Combination (Board + Live)</strong></td>
                    <td>53.3%</td>
                    <td><em>"I like both methods. Going through prewritten code gives me the opportunity to really focus. Writing live code gives me the opportunity to see the execution."</em></td>
                </tr>
                <tr>
                    <td><strong>Whiteboard</strong></td>
                    <td>46.7%</td>
                    <td><em>"Writing on the white board is easier...breaking down code point by point allows me to grasp each part."</em></td>
                </tr>
                <tr>
                    <td><strong>Pre-written</strong></td>
                    <td>26.7%</td>
                    <td><em>"Pre-written examples seem clearer. Live coding gets confusing."</em></td>
                </tr>
                <tr>
                    <td><strong>Live Coding</strong></td>
                    <td>13.3%</td>
                    <td><em>"Live coding works better for me...it slows everything down so I can digest the material."</em></td>
                </tr>
            </tbody>
        </table>
    </div>
</div>

**Best Practice:** Write a long example on the board → trace its execution in a memory diagram → project its execution in a code interpreter.

### 5. 🎯 Use Relevant Examples

<div class="alert alert-warning mt-3" role="alert">
    <h6 class="alert-heading text-dark"><i class="fas fa-lightbulb"></i> Andragogy Principle</h6>
    <p class="small mb-0 text-dark">Adult learners want to understand the value of learning something before investing effort. Incorporate culturally relevant examples that connect to students' diverse life experiences and backgrounds.</p>
</div>

### 6. 🎤 Make Use of High Engagement in Lecture

Peer Instruction worked exceptionally well:

- Students were **cooperative and self-organized**
- Higher-performing students naturally moved to sit with struggling peers
- Students engaged in **productive discussion** about differing opinions
- Course evaluations highlighted this as particularly helpful

### 7. 📚 Students are Skilled Independent Learners

Many incarcerated students had extensive experience with self-teaching through correspondence courses:

<div class="alert alert-success mt-2" role="alert">
    <p class="small mb-0 text-dark"><strong class="text-dark">Implication:</strong> Provide substantial resources for learning outside class—textbook readings, written materials, and video tutorials (given varying access to laptops).</p>
</div>

### 8. 🎨 Create Opportunities for Self-Expression

Beyond required assignments, we allowed students to submit any code written for practice or fun:

- We transcribed the code, printed the output, and delivered it back
- Many students (both high and low performers) took advantage
- Programs were often personal and creatively expressive
- **Future direction:** Encourage creative expression more explicitly

## Impact & Implications

<div class="row mt-3">
    <div class="col-md-6">
        <h5><i class="fas fa-graduation-cap"></i> For Computing Education</h5>
        <ul class="small">
            <li>Demonstrates feasibility of CS education in constrained environments</li>
            <li>Brings diverse perspectives into computing</li>
            <li>Expands equitable access to computing careers</li>
            <li>Benefits both students and the computing field</li>
        </ul>
    </div>
    <div class="col-md-6">
        <h5><i class="fas fa-users"></i> For Future Prison Programs</h5>
        <ul class="small">
            <li>Leverage student maturity and community</li>
            <li>Design for limited resources creatively</li>
            <li>Adapt teaching methods based on feedback</li>
            <li>Recognize and celebrate student strengths</li>
        </ul>
    </div>
</div>

## Publication

This work was published in the **Proceedings of the 55th ACM Technical Symposium on Computer Science Education (SIGCSE 2024)**:

*Hogan, E., Li, R., Soosai Raj, A. G., Griswold, W. G., & Porter, L. (2024). Challenges and Approaches to Teaching CS1 in Prison.*

<div class="row mt-3">
    <div class="col-md-6">
        <a href="assets/pdf/cs1_prison.pdf" class="btn btn-info btn-block" target="_blank">
            <i class="fas fa-file-pdf"></i> Read the Paper
        </a>
    </div>
    <div class="col-md-6">
        <a href="https://dl.acm.org/doi/10.1145/3626252.3630802" class="btn btn-primary btn-block" target="_blank">
            <i class="fas fa-external-link-alt"></i> ACM Digital Library
        </a>
    </div>
</div>
