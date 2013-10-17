---
layout: pagewithsidebar
title:  Dark Energy Science Collaboration Software Workbook
---

<!---
Note: You can put comments into the markdown code like this.  You can
also use this notation to comment out sections of the code.  This can
also be useful for debugging in case the pages don't build for some reason.
-->

##<span class="pictos">n</span> Introduction

This site is a workbook/wiki for introducing LSST DESC software
including the Data Managment Stack (DM). It is hosted on github along
with a set of ipython notebooks that are used in the tutorials.  You
can edit this page and also add and edit the ipython notebooks
themselves.  See the links on the right hand side for instruction on
how to edit the pages.

Currently, this site contains a set up DM tutorials.  Each tutorial
has been implemented as an [iPython][ipython] notebook. For each
iPython notebook there is a link that will allow you to view them in a
read-only mode in your web browser.  A link is also provided to the
notebook itself (which is hosted on github) if you would like to
run them yourself and modify them etc.

[ipython]: http://ipython.org

##<span class="pictos">n</span> Data Management (DM) Tutorials

For people new to DM it can be difficult to understand how to get
started.  This is especially true when trying to do basic operations
on images.  These tutorials are designed to show how basic operations
on images work, and then, how the various pieces are put together into
the command line tasks that are included in DM.  Understanding these
tutorials should allow you both to write your own commandline tasks
and write DM code which either leverages the default algorithms, or is
not reliant on them at all.  For those who just want to use the
included commandline tasks the tutorials should also serve to help you
understand how they actually work.  Even when these tutorials are not
completely explanatory, when coupled with some of the official
documentation they will give you examples of working code.

### Basic Operations

This example notebook is a basic introduction to the operations in the
Applications Framework (AFW) section of DM.  The notebook covers the
usage of creating basic exposures and doing pixel level statistics
including using masks.  Then, manually controlling and calling
algorithms for detection and measurement are introduced.  

Note that running this tutorial yourself requires you to have a PhoSim
output file.  To produce this you can follow the "PhoSim walkthrough"
referenced below.  If you can't, or don't want to do that, a sample
file is also available immediately below.  Also, to run the tutorials
yourself you should have installed and setup the DM stack.  See the
_External Links_ section below if you don't know how to do this.  In
order for the tutorials to work you should "setup" both pipe_tasks and
obs_llstSim.

* __View a read-only web version of the notebook [here][nbviewer#1] and download  a local copy of the  notebook [here][rawnotebook#1]__
* A copy of the phosim file used in the introduction notebook is
 [here][phosimFile]. You should download this file if you want to run
 the  notebooks and have not created it yourself by running phosim.
 
[nbviewer#1]:        http://nbviewer.ipython.org/url/raw.github.com/cwwalter/DESCSoftwareWorkBook/master/Basic%20DM%20AFW%20Introduction.ipynb "Intro to AFW"
[rawnotebook#1]: https://rawgithub.com/cwwalter/DESCSoftwareWorkBook/master/Basic%20DM%20AFW%20Introduction.ipynb
[phosimFile]:         https://rawgithub.com/cwwalter/DESCSoftwareWorkBook/gh-pages/files/lsst_e_99999999_f2_R22_S11_E000.fits.gz

### Tables and Catalogs

This short notebook contains a basic introduction to the "Tables" and "Catalogs" in
DM. They are a heavily used feature in the detection and
characterization algorithms and work somewhat differently than the
standard container classes you might be used to.

* __View a web version of the notebook [here][nbviewer#2] and download  a local copy of the  notebook [here][rawnotebook#2]__

[nbviewer#2]:       http://nbviewer.ipython.org/url/raw.github.com/cwwalter/DESCSoftwareWorkBook/master/Table%20and%20Catalog%20Introduction.ipynb

[rawnotebook#2]: https://rawgithub.com/cwwalter/DESCSoftwareWorkBook/master/Table%20and%20Catalog%20Introduction.ipynb

### Command Line Tasks

This notebook is an introduction to pipeline tasks.  These are the
example executables included in DM for high level processing.  We will
build a pipeline task from the ground up based on the previous example
notebooks so you can see how they are implemented. Note to run these
as a notebook you will need to have rearranged your phosim output as
explained by the link in the _External References_ below.

* __View a web version of the notebook [here][nbviewer#3] and download  a local copy of the  notebook [here][rawnotebook#3]__

[nbviewer#3]: http://nbviewer.ipython.org/url/raw.github.com/cwwalter/DESCSoftwareWorkBook/master/Command%20Line%20Task.ipynb

[rawnotebook#3]: https://rawgithub.com/cwwalter/DESCSoftwareWorkBook/master/Command%20Line%20Task.ipynb

### Useful topics that are not yet covered

There are several topics and concepts that are not covered here.  Why
don't you write one!  Here is a short list of some suggested
tutorials:

* Accessing and interfacing with the CatSim catalog.
* Controlling command line tasks with argument parsers and config files.

##<span class="pictos">n</span> External References

In this section useful external references are listed.  In many cases
the information in these links are out-of-date and contain incorrect
information.  If there is a conflict you should use the information on
this page.  However, even those pages can still be useful to
understand certain concepts in the software.  These are the pages that
were useful to Chris Walter (CWW) when learning how to use the
software and putting together these pages.

### Getting Started 

* The official development portal for the DM software is on the [LSST
  Corporation Trac][trac].
* Documentation which is automatically generated from the source code
  itself including the class structures etc can be found [here][doxygen].
* Instructions for installing a local copy of DM can be found
  [here][DMinstall].  The instructions for the 2013 versions used by
  CWW for the notebooks above are [here][DM2013].
* A software manual from 2011 can be found [here][lsstManual-2011].   
  _[CWW: This is old and out of data but the first chapter is very
  useful.  The pipeline described in this document is no longer used
  and should be ignored]_
* The LSST Data Challenge Handbook (v1.1) can be found
  [here][handbook_v1.1]. This version is old, there are newer versions
  available.  However, this version is quite useful to
  newcomers.  That is because it explains the naming conventions for
  visits and filters and something about the relationship between
  different types of exposures.  It also explains the LSST focal plane
  sensor numbering scheme.

DESC members can access the following link on the [SLAC confluence][confluence]:
 
* The Weak Lensing group's [Basic References for DESC][WLrefs]

[trac]:                      https://dev.lsstcorp.org/trac
[DMinstall]:            https://dev.lsstcorp.org/trac/wiki/Installing
[DM2013]:               https://dev.lsstcorp.org/trac/wiki/Installing/Summer2013
[lsstManual-2011]: https://dev.lsstcorp.org/trac/attachment/wiki/Applications/lsstManual.pdf
[handbook_v1.1]:    https://dev.lsstcorp.org/trac/wiki/DC3bUserGuide
[doxygen]:             http://lsst-web.ncsa.illinois.edu/doxygen/x_masterDoxyDoc/

[confluence]:         https://confluence.slac.stanford.edu/display/LSSTDESC/Home
[WLrefs]:                https://confluence.slac.stanford.edu/display/LSSTDESC/Basic+references+for+DESC+WL

### Phosim

* You can find phosim info [here][phosim]
* A copy of the PhoSim manual can be found here (need public link).

DESC members can access the following link on the [SLAC confluence][confluence]:
 
* A phosim [walkthrough][descphosim]
 
[phosim]:              https://dev.lsstcorp.org/trac/wiki/IS_phosim
[descphosim]:      https://confluence.slac.stanford.edu/display/LSSTDESC/phoSim+Walkthrough

### DM 

* Some documentation on dataButlers and accessing data and exposures can be found [here][butler] and
  [here][butler2].
* The philosophy behind the AFW table code is explained [here][table].
* [This][imsimpipeline] page explains how to move the phosim output around so that you
  can use DM databutlers on them.  
   _[CWW: Be careful getting the daf  code.  You should actually get this code from the GIT repository
   (LSST/DMS/daf_replicate.git) not the SVN repository. Also the filename structure has changed so you
   will need to tweak the vdist_pt1_1.py script.]_
* [Here][advanced] is an advanced example of using DM pipelines to
  process the SDSS [stripe 82][stripe82] data.  
  _[CWW: I haven't checked this]_

[butler]:                https://dev.lsstcorp.org/trac/wiki/v62_processCCD_data
[butler2]:                https://dev.lsstcorp.org/trac/wiki/DataButler
[table]:                  https://dev.lsstcorp.org/trac/wiki/Winter2012/NewSourceFAQ
[imsimpipeline]:  http://kipac.stanford.edu/collab/research/lensing/slac/HowTo/imsimDMpipeline
[advanced]:           https://dev.lsstcorp.org/trac/wiki/Summer2013/ConfigAndStackTestingPlans/Instructions
[stripe82]:             http://www.physics.drexel.edu/~gtr/vla/stripe82/Deep_VLA_Observations_of_SDSS_Stripe_82.html
