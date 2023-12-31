---
layout: page
title: DFT Investigation of 2D Nanomaterials
description: Computational Investigation of 2D monolayer and heterostructures materials' electronic and optical properties using First-Principles Density Functional Theorem (DFT)
img: assets/img/DFT-project/dft-thumb.png
importance: 1
category: research
related_publications: mojumder2022tunable, mojumder2021germanene, mojumder2020electronic, islam2021germanene, 
---

* Germanene/2D-GaP hetero-bilayer structure: scf and bands calculation (Quantum Espresso codes)"
  
    (i) GeGaP.scf.in 
    ```html
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
    ```
    (ii) GeGaP.b-nscf.in
    ```html
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
    ```
    (iii) GeGaP.band.in
    ```html
		&bands
		outdir = "./work/"
		prefix = 'GaP+Ge_I_3.70'
		filband = 'GaP+Ge_I_3.70.band'
		lsym = .true.
		/
    ```

Now, let's see some of the outputs. First, the scf and band outputs for the considered gemranene/2D-AlP hetero-bilayer is provided below. <br> <br>
To view image in full size => <u><b><i>Open image in new tab</i></b></U> 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-4.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>
<ul style='text-align: justify;'>
  <li>Left - Four stacking arrangements of the germanene/2D-AlP heterostructure at equilibrium (a) pattern-I, (b) pattern-II, (c) pattern-III, and (d) pattern-IV. A typical side view of the heterobilayer is placed in the center. “h” denotes the interlayer separation, and “Δ” denotes the buckling height.</li>
  <li>Middle - The variation of binding energy/Ge atom as a function of the interlayer separation for the four patterns of germanene/2D-AlP heterobilayers. Downward arrows indicate the optimized interlayer distances for the respective patterns.</li>
  <li>Right - Band diagrams and associated density of states (DOS) for germanene/2D-AlP heterobilayers for (a) pattern-I, (b) pattern-II, (c) pattern-III, and (d) pattern-IV.</li>
</ul>
</b>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-5.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-6.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-7.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>
<ul style='text-align: justify;'>
  <li>Left - Band structures of the germanene/2D-AlP heterobilayer with SOC (a) pattern-I, (b) pattern-II, (c) pattern-III, and (d) pattern-IV. </li>
  <li>Middle - (a) Atom projected density of states (PDOS) and (b) orbital projected density of states (PDOS) for pattern-III of the germanene/2D-AlP heterobilayer. Fermi level is set at 0.</li>
  <li>Right - (a) Space charge density and (b) charge density difference (CDD) for pattern-III of the germanene/2D-AlP heterobilayer. The isovalue is 0.00187 e/Å3. (VB - Valence Band and CB- Conduction Band).</li>
</ul>
</b>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-9.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-10.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DFT-project/fig-13.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
<b>
<ul style='text-align: justify;'>
  <li>Left - The variation of the bandgap and effective mass of the electron as a function of tensile strain (+ve) and compressive strain (−ve) for pattern-III of the germanene/2D-AlP heterobilayer. </li>
  <li>Middle - The bandgap and electron mobility variation as a function of the applied electric field for pattern-III of the germanene/2D-AlP heterobilayer. The direction of the applied positive electric field is from the 2D-AlP monolayer toward the germanene monolayer.</li>
  <li>Right - (a) Phonon dispersion relation and (b) vibrational density of states (VDOS) of pattern-III of the germanene/2D-AlP heterobilayer.</li>
</ul>
</b>
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

