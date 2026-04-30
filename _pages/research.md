---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

<style>
/* Scope page-only image rules so they don't affect header/nav icons */
#gridid img{
  border-radius: 10px;
  /* float: left; */
  padding: 15px;
}
#gridid .col-md-3 {
  margin-top:10px;
  margin-bottom:10px;
  padding:0px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  background: white;
  border-radius: 20px;
  height: auto;
}
#gridid iframe {
  margin:0;
  padding:0;
  width: 175px;
  display: inline;
  vertical-align: middle;
}
</style>

## Research

<div class="jumbotron">
<div class="col-md-12 col-sm-12" >
<h4>MDPD-Martini Force-Field</h4>

<img src="/images/martini.png" alt="MDPD-Martini lipid membrane" width=320 style="float: left">


MDPD-Martini is a coarse-grained force field that integrates the many-body dissipative particle dynamics (MDPD) method with the MARTINI coarse-graining approach. It accurately simulates liquid-vapor interfaces and surface tension by having MDPD's density-dependent pairwise non-bonded interactions. This enables the accurate and stable simulation of liquid droplets, lipid membranes, and surfactant assemblies in aqueous environments, making it particularly powerful for studying phenomena like vesicle self-assembly, emulsion stability, and the dynamics of soft matter systems where interfacial physics are critical. Due to MDPD's soft potential, it also offers a possible advantage in computational cost due to larger simulation time-steps when compared to molecular dynamics.


</div></div>

<div class="jumbotron">
<div class="col-md-12 col-sm-12" >
<h4>Liquid jet breakup</h4>

<img src="/images/break.png" alt="RP break" width=320 style="float: left">

In fluid dynamics, the liquid jet breakup problem is described by the Rayleigh–Plateau instability. This instability is driven by surface tension, which tries to minimize the surface energy of a cylindrical liquid jet and eventually break it into droplets. Continuum analysis with the Navier–Stokes equations yields a dispersion relation for the growth rate of different perturbation wavelengths based on the Ohnesorge number. However, at small enough scales, thermal fluctuations become strong enough that they can affect the breakup dynamics. We showed through mesoscale particle simulations (MDPD) that the breakup of a liquid thread under thermal fluctuations is driven by the most unstable wavelength predicted by the continuum theory. Furthermore, we incorporated a molecular surfactant model and showed a transition in pinching dynamics as a function of concentration.



</div></div>

<div class="jumbotron">
<div class="col-md-12 col-sm-12" >
<h4>ALE/FEM Stream function-voticity (MSc Project)</h4>

<img src="/images/msc-vort.png" alt="alefem" width=640>

</div></div>
