---
layout: page
title: Merge Sort on FPGA
description: Design of an IP block for Merge Sort acceleration on PYNQ-Z2 FPGA
img: assets/img/fpga.jpg
importance: 1
category: university
---
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/fpga.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Introduction
<p align="justify">
I have designed three different IP block for Merge Sort acceleration on FPGA for the FPGA101 PiA Course Project by Politecnico di Milano. The first design that was formulated consists in a cascade tree of comparators, the second in a row of comparators orchestrated by a Finite State Machine. Both designs achieved a 16x speedup w.r.t. the Python SW implementation of the algorithm. Lastly, a hybrid approach was adopted where a smaller comparator tree was managed by a FSM, reducing HW consumption and yielding a 25x speedup.
</p>

### Github Directories

The repo contains three different folders for each architecture experimented, namely tree, row, hybrid, a pdf report describing the proceudre adopted and the results obtained and, lastly, a jupyter notebook to run the final designs on the PYNQ-Z2 FPGA and compare their performances with the SW algorithm implementation.

