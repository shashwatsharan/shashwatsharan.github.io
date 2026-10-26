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

{% comment %}
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
{% endcomment %}

2022
: Academic Excellence in Mathematics Award, San Diego State University

2022
: Master's Research Scholarship, San Diego State University

## Talks and presentations

#### Invited seminars and conference talks

Mar 2027<br><small>(upcoming)</small>
: <span class="loc">Athens, GA, USA</span>Waves 2027<br>
<span class="session">Minisymposium: Regular and Stochastic Dispersive Hydrodynamics, University of Georgia</span>

Nov 2026
: <span class="loc">Tempe, AZ, USA</span>AMS Fall Western Sectional Meeting<br>
<span class="session">Special Session on Nonlinear Waves, Integrable Systems, and Inverse Scattering</span>

Oct 2026
: <span class="loc">Dallas, TX, USA</span>SIAM Texas–Louisiana Section Annual Meeting<br>
<span class="session">Minisymposium MS39: Recent Advances in Nonlinear Waves and Integrable Systems</span>

May 2026
: <span class="loc">Montréal, Canada</span>SIAM Conference on Nonlinear Waves and Coherent Structures (NWCS26)<br>
<span class="session">Minisymposium MS19: Recent Advances in Dispersive Hydrodynamics</span> {% comment %}<br>*Breaking a Superfluid Harmonic Dam: Rarefaction Dynamics of a Trapped Condensate*{% endcomment %}

Nov 2025
: <span class="loc">Boulder, CO, USA</span>Nonlinear Waves Seminar<br>
<span class="session">Department of Applied Mathematics, CU Boulder</span> {% comment %}<br>*Vacuum dambreak of a superfluid: rarefaction waves in harmonic potential*{% endcomment %}

Mar 2025
: <span class="loc">Lawrence, KS, USA</span>AMS Spring Central Sectional Meeting<br>
<span class="session">Special Session on Dispersive Hydrodynamics, University of Kansas</span> {% comment %}<br>*Vacuum dam break problem for the defocusing NLS equation with a harmonic potential*{% endcomment %}

Mar 2018
: <span class="loc">Vellore, India</span>International Seminar on Emerging Trends in Mathematics<br>
<span class="session">Vellore Institute of Technology</span> {% comment %}<br>*N-body gravitational simulations and trajectories around rotating spherical bodies*{% endcomment %}

#### Contributed talks

Apr 2025
: <span class="loc">Athens, GA, USA</span>Waves 2025<br>
<span class="session">University of Georgia</span><br>
*Dry dam break of a confined Bose–Einstein condensate*

Jan 2025
: <span class="loc">Seattle, WA, USA</span>Joint Mathematics Meetings (JMM 2025)<br>
<span class="session">Seattle Convention Center</span><br>
*Dry dam break of a confined Bose–Einstein condensate*

#### Posters

Oct 2025
: <span class="loc">Berkeley, CA, USA</span>2nd SIAM Northern and Central California Sectional Conference (NCC25)<br>
<span class="session">Lawrence Berkeley National Laboratory</span><br>
*Dam break dynamics of a confined Bose–Einstein condensate*

Oct 2024
: <span class="loc">Merced, CA, USA</span>1st SIAM Northern and Central California Sectional Conference (NCC24)<br>
<span class="session">UC Merced</span><br>
*Dam break dynamics of a confined Bose–Einstein condensate*

Jul 2024
: <span class="loc">Newcastle, UK</span>Workshop on Emergent Phenomena in Nonlinear Dispersive Waves<br>
<span class="session">Northumbria University</span><br>
*Riemann problem for spin coupled Bose–Einstein condensates*

Jun 2024
: <span class="loc">Baltimore, MD, USA</span>SIAM Conference on Nonlinear Waves and Coherent Structures (NWCS24)<br>
<span class="session">Lord Baltimore Hotel</span><br>
*Riemann problem for spin coupled Bose–Einstein condensates*

May 2022
: <span class="loc">Claremont, CA, USA</span>Southern California Applied Mathematics Symposium (SoCAMS)<br>
<span class="session">Harvey Mudd College</span><br>
*Dynamics and bifurcations of feedforward networks*

#### Invited workshops

Jun 2026
: <span class="loc">Trieste, Italy</span>ICTP-INdAM-SLMath Summer Graduate School for Machine Learning<br>
<span class="session">International Centre for Theoretical Physics (ICTP)</span>

Jul 2024
: <span class="loc">Newcastle, UK</span>Workshop on Emergent Phenomena in Nonlinear Dispersive Waves<br>
<span class="session">Northumbria University</span>

## Service and outreach

2025 – 26
: **Preliminary Exam Coach**, UC Merced. Organised and led problem-solving sessions for graduate students preparing for preliminary examinations.

Fall 2025
: **Graduate Peer Mentor**, UC Merced. Supported incoming graduate students with academic guidance and advice on coursework, teaching and workload.

2017 – 20
: **Projects Team, VIT Mathematical Association**. Represented the university in the COMAP MCM and ICM modelling competitions; recruited and mentored student teams.
