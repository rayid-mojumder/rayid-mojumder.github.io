---
layout: page
title: DFT Investigation of 2D Nanomaterials
description: Computational Investigation of 2D monolayer and heterostructures materials' electronic and optical properties using First-Principles Density Functional Theorem (DFT)
img: assets/DFT-project/dft-thumb.png
importance: 1
category: research
related_publications: einstein1956investigations, einstein1950meaning
---

* Germanene/2D-AlP hetero-bilayer structure: scf and bands calculation (Quantum Espresso codes)"
    (i) GeAlP.scf.in 
    ---
		&CONTROL
		calculation = "scf"
		outdir = "./work/"
		prefix = "GaP+Ge_I_3.70"
		pseudo_dir = "./pseudo/"
		restart_mode = "from_scratch"
		verbosity = 'high'
		/
		&SYSTEM
		ibrav = 4
		a = 3.89
		c = 20
		nat = 4
		ntyp = 3
		ecutwfc = 30.0,
		ecutrho = 120.0,
		occupations = 'smearing'
		smearing = 'm-p'
		degauss = 0.0005
		input_dft = 'pbe'
		vdw_corr = 'Grimme-D2',
		/
		&ELECTRONS
		© Md. Rayid Hasan Mojumder
		28
		conv_thr = 1.00000e-8
		mixing_beta = 0.7
		/
		ATOMIC_SPECIES
		Ga 69.723 Ga.pbe-mt_fhi.UPF
		P 30.973762 P.pbe-mt_fhi.UPF
		Ge 72.64 Ge.pbe-mt_fhi.UPF
		ATOMIC_POSITIONS (angstrom)
		Ga 0.000000000 0.000000000 0.000000
		P 0.000000000 2.245892547 0.380000
		Ge 0.000000000 0.000000000 3.70
		Ge 0.000000000 2.245892547 4.08
		K_POINTS {automatic}
		10 10 1 0 0 0		
    ---
    (ii) GeAlP.b-nscf.in
    ---
		&CONTROL
		calculation = "bands"
		outdir = "./work/"
		prefix = "GaP+Ge_I_3.70"
		pseudo_dir = "./pseudo/"
		restart_mode = "from_scratch"
		verbosity = 'high'
		/
		&SYSTEM
		ibrav = 4
		a = 3.89
		c = 20
		nat = 4
		ntyp = 3
		ecutwfc = 30.0,
		ecutrho = 120.0,
		occupations = 'smearing'
		smearing = 'm-p'
		degauss = 0.0005
		input_dft = 'pbe'
		vdw_corr = 'Grimme-D2',
		/
		&ELECTRONS
		conv_thr = 1.00000e-8
		mixing_beta = 0.7
		/
		ATOMIC_SPECIES
		© Md. Rayid Hasan Mojumder
		29
		Ga 69.723 Ga.pbe-mt_fhi.UPF
		P 30.973762 P.pbe-mt_fhi.UPF
		Ge 72.64 Ge.pbe-mt_fhi.UPF
		ATOMIC_POSITIONS (angstrom)
		Ga 0.000000000 0.000000000 0.000000
		P 0.000000000 2.245892547 0.380000
		Ge 0.000000000 0.000000000 3.70
		Ge 0.000000000 2.245892547 4.08
		K_POINTS {crystal_b}
		4
		0.0000000 0.0000000 0.0000000 20 !G
		0.3333333 0.3333333 0.0000000 20 !k
		0.0000000 0.5000000 0.0000000 20 !M
		0.0000000 0.0000000 0.0000000 20 !G	
    ---
    (iii) GeAlP.band.in
    ---
		&bands
		outdir = "./work/"
		prefix = 'GaP+Ge_I_3.70'
		filband = 'GaP+Ge_I_3.70.band'
		lsym = .true.
		/
    ---


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-1.jpeg" title="Four stacking arrangements of the germanene/2D-AlP heterostructure at equilibrium (a) pattern-I, (b) pattern-II, (c) pattern-III, and (d) pattern-IV. A typical side view of the heterobilayer is placed in the center. “h” denotes the interlayer separation, and “Δ” denotes the buckling height." class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-2.jpeg title="The variation of binding energy/Ge atom as a function of the interlayer separation for the four patterns of germanene/2D-AlP heterobilayers. Downward arrows indicate the optimized interlayer distances for the respective patterns." class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-4.jpeg" title="Electronic band diagram of (a) germanene without SOC, (b) germanene with SOC, and (c) monolayer AlP." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Optimized four stacking structure of the Germanene/2D-AlP hetero-bilayers and observed bandgaps.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-5.jpeg" title="Band structures of the germanene/2D-AlP heterobilayer with SOC (a) pattern-I, (b) pattern-II, (c) pattern-III, and (d) pattern-IV." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Spin-Orbit Coupling (SOC) increases the bandgaps for the heterobilayer structures.
</div>

To analyze the density of states (DOS) in a bit more insightful manner, the total and the atom projected density of states (PDOS) are detailed in this portion. Also, charge density difference (CDD) and charge density distribution are depicted.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-6.jpeg" title="(a) Atom projected density of states (PDOS) and (b) orbital projected density of states (PDOS) for pattern-III of the germanene/2D-AlP heterobilayer. Fermi level is set at 0." class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-7.jpeg" title="(a) Space charge density and (b) charge density difference (CDD) for pattern-III of the germanene/2D-AlP heterobilayer. The isovalue is 0.00187 e/Å3. (VB - Valence Band and CB- Conduction Band)." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    As you can see the germanene layer dominates and controls the carrier mobility, thus low effective mass could be observed.
</div>

Now, see how the bandgap could be engineered using external biaxial strain and changing the interlayer spacing between the germanene and 2D-AlP layer:

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-9.jpeg" title="The variation of the bandgap and effective mass of the electron as a function of tensile strain (+ve) and compressive strain (−ve) for pattern-III of the germanene/2D-AlP heterobilayer." class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-10.jpeg" title="The bandgap and electron mobility variation as a function of the applied electric field for pattern-III of the germanene/2D-AlP heterobilayer. The direction of the applied positive electric field is from the 2D-AlP monolayer toward the germanene monolayer." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left- Strain engineering. Right - interlayer spacing engineering.
</div>

Finally, lets see the phonon dispersion for germanene/2D-AlP heterostructure pattern III

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-13.jpeg" title="(a) Phonon dispersion relation and (b) vibrational density of states (VDOS) of pattern-III of the germanene/2D-AlP heterobilayer." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Optical and acoustic phonon frequencies.
</div>


<!--- I am commenting out this part. To uncomment discard the html comments notations)
The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
-->

