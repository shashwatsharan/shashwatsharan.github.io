---
layout: default
title: Curriculum Vitae
---

{% assign cv = site.static_files | where: "path", "/assets/cv.pdf" | first %}
{% if cv %}<p><a href="{{ '/assets/cv.pdf' | relative_url }}">Download the full CV (PDF)</a></p>{% endif %}

## Education

2022 – 2026
: **PhD, Applied Mathematics**, University of California, Merced<br>
Thesis: *Dambreak Hydrodynamics of Confined Bose–Einstein Condensates*.<br>
Advisor: Prof. Boaz Ilan

2020 – 2022
: **MS, Applied Mathematics**, San Diego State University<br>
Thesis: *Dynamics and Bifurcations of Feedforward Networks*.<br>
Advisor: Prof. Antonio Palacios

2016 – 2020
: **B.Tech, Electrical and Electronics Engineering**, Vellore Institute of Technology<br>
Capstone: *Design of Control Systems for Inverted Double Linear and Rotary Pendulums*.<br>
Advisor: Prof. Rashmi Ranjan Das

## Employment

2026 –
: Keith Julien Visiting Assistant Professor, University of Colorado Boulder

Summer 2026
: Teaching Fellow, University of California, Merced

2022 – 2026
: Graduate Teaching Assistant, University of California, Merced

Spring 2022
: Graduate Research Assistant, SDSU Research Foundation

Fall 2021
: Graduate Teaching Associate, San Diego State University

## Publications and teaching

See [Publications](/publications/) and [Teaching](/teaching/).

{% assign rs = site.static_files | where: "path", "/assets/research-statement.pdf" | first %}
{% assign ts = site.static_files | where: "path", "/assets/teaching-statement.pdf" | first %}
{% if rs or ts %}
## Statements

{% if rs %}<p><a href="{{ '/assets/research-statement.pdf' | relative_url }}">Research statement (PDF)</a></p>{% endif %}
{% if ts %}<p><a href="{{ '/assets/teaching-statement.pdf' | relative_url }}">Teaching statement (PDF)</a></p>{% endif %}
{% endif %}

## Awards and honours

2026
: Applied Mathematics Excellence in Research Award, UC Merced

2026
: Applied Mathematics Distinguished Service Award, UC Merced
<!--
2024 – 26
: Applied Mathematics Summer Fellowship, UC Merced (2024, 2025, 2026)

2024, 2026
: Applied Mathematics Travel Award, UC Merced

2025
: GradEXCEL Peer Mentor Award, UC Merced

2024
: Graduate Student Association Travel Award Fellowship, UC Merced

2024
: MacKenzie Scott Graduate Travel Award, UC Merced
-->

2022
: Academic Excellence in Mathematics Award, San Diego State University

2022
: Master's Research Scholarship, San Diego State University

## Talks and presentations

#### Invited seminars and conference talks

May 2026
: *Breaking a Superfluid Harmonic Dam: Rarefaction Dynamics of a Trapped Condensate*<br>
SIAM Conference on Nonlinear Waves and Coherent Structures (NWCS26), Minisymposium MS19: Recent Advances in Dispersive Hydrodynamics, Montréal, Canada

Nov 2025
: *Vacuum dambreak of a superfluid: rarefaction waves in harmonic potential*<br>
Nonlinear Waves Seminar, Department of Applied Mathematics, CU Boulder

Mar 2025
: *Vacuum dam break problem for the defocusing NLS equation with a harmonic potential*<br>
AMS Spring Central Sectional Meeting, Special Session on Dispersive Hydrodynamics, University of Kansas

Mar 2018
: *N-body gravitational simulations and trajectories around rotating spherical bodies*<br>
International Seminar on Emerging Trends in Mathematics, VIT Vellore, India

#### Contributed talks and posters

Apr 2025
: *Dry dam break of a confined Bose–Einstein condensate* <span class="tag">talk</span><br>
13th International Conference on Nonlinear Evolution Equations and Wave Phenomena, Athens, GA

Jan 2025
: *Dry dam break of a confined Bose–Einstein condensate* <span class="tag">talk</span><br>
Joint Mathematics Meetings (JMM 2025), Seattle, WA

Oct 2024
: *Dam break dynamics of a confined Bose–Einstein condensate* <span class="tag">poster</span><br>
SIAM Northern California Conference, UC Merced

Jul 2024
: *Riemann problem for spin coupled Bose–Einstein condensates* <span class="tag">poster</span><br>
Workshop on Emergent Phenomena in Nonlinear Dispersive Waves, Newcastle, UK

Jun 2024
: *Riemann problem for spin coupled Bose–Einstein condensates* <span class="tag">poster</span><br>
SIAM Conference on Nonlinear Waves and Coherent Structures, Baltimore, MD

May 2022
: *Dynamics and bifurcations of feedforward networks* <span class="tag">poster</span><br>
Southern California Applied Mathematics Symposium, Harvey Mudd College

#### Invited workshops

Jun 2026
: ICTP-INdAM-SLMath Summer Graduate School for Machine Learning, ICTP, Trieste, Italy

Jul 2024
: Workshop on Emergent Phenomena in Nonlinear Dispersive Waves, Northumbria University, Newcastle, UK

## Service and outreach

2025 – 26
: **Preliminary Exam Coach**, UC Merced. Organised and led problem-solving sessions for graduate students preparing for preliminary examinations.

Fall 2025
: **Graduate Peer Mentor**, UC Merced. Supported incoming graduate students with academic guidance and advice on coursework, teaching and workload.

2017 – 20
: **Projects Team, VIT Mathematical Association**. Represented the university in the COMAP MCM and ICM modelling competitions; recruited and mentored student teams.
