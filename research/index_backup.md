---
layout: default
title: Research
published: false
---
**To learn about our current research activities, please read the [recent publications](\research\publications). While we try our best to keep things updated, the following project descriptions may not be the most up-to-date.**

<div class="alert alert-warning">
    Click on the project titles for more information!
</div>

<!--

Add "in" to the end of       <div id="n-path" class="panel-collapse collapse"> to make a section expanded by default
e.g.       <div id="n-path" class="panel-collapse collapse in">
-->

### Active Circuits

<div class="panel-group" id="actives">

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#circuits" href="#n-path">Tunable N-Path Integrated Filters with Enhanced Block Rejection</a>
        </h4>
      </div>
      <div id="n-path" class="panel-collapse collapse">
        <div class="panel-body">
    {% include_relative /npath-filter/n-path.html %}
        </div>
      </div>
    </div>

</div>

### Passive Devices
<div class="panel-group" id="passives">

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#circuits" href="#tunable-filter">High-Q Tunable Evanescent-mode Cavity Filters</a>
        </h4>
      </div>
      <div id="tunable-filter" class="panel-collapse collapse">
        <div class="panel-body">
    {% include_relative /tunable-filter/tunable-filter.html %}
        </div>
      </div>
    </div>

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#devices" href="#hot-rfmems">Highly Reliable Hot-Switching RF-MEMS Switches</a>
        </h4>
      </div>
      <div id="hot-rfmems" class="panel-collapse collapse">
        <div class="panel-body">
		{% include_relative /rfmems/hot-rfmems.html %}
        </div>
      </div>
    </div>

 <!--   
    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#devices" href="#mems-rectf">Resonant Voltage Amplification for Extremely Low-power RF signal Detection and Conversion</a>
        </h4>
      </div>
      <div id="mems-rectf" class="panel-collapse collapse">
        <div class="panel-body">
    		{% include_relative mems-rectifier.html %}
        </div>
      </div>
    </div>
-->

</div>


### Systems
<div class="panel-group" id="systems">

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#devices" href="#thzi">High-speed Chip-to-chip Interconnects at Sub-millimeter-wave and THz Frequencies</a>
        </h4>
      </div>
      <div id="thzi" class="panel-collapse collapse">
        <div class="panel-body">
		{% include_relative /thz-inter/thz-inter.html %}
        </div>
      </div>
    </div>

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#system" href="#bps">Reconfigurable Bandpass Sampling Receivers for Software-Defined Radio Applications</a>
        </h4>
      </div>
      <div id="bps" class="panel-collapse collapse">
        <div class="panel-body">
		{% include_relative /bpsr/tunable-bps.html %}
        </div>
      </div>
    </div>

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#system" href="#cardiac">Wearable Radar Sensor for Long-term Cardiac Arrhythmia Monitoring</a>
        </h4>
      </div>
      <div id="cardiac" class="panel-collapse collapse">
        <div class="panel-body">
    		{% include_relative /cardiac-radar/cardiac-radar.html %}
        </div>
      </div>
    </div>

</div>

### Archived

<div class="panel-group" id="archieved">

    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title">
          <a data-toggle="collapse" data-parent="#archived" href="#tunable-power">Electro-Mechancial Instability in MEMS-enabled Tunable Evanescent-mode High-frequency filters</a>
        </h4>
      </div>
      <div id="tunable-power" class="panel-collapse collapse">
        <div class="panel-body">
		{% include_relative /tunable-filter/tunable-power.html %}
        </div>
      </div>
    </div>

</div>
