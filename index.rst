####################################################
Non-Quality Performance Metrics for DM in Operations
####################################################

.. abstract::

   A concise  set of performance metrics that are tracked by the team and reported to operations management


Non-Scientific Performance Metrics for Operations
=================================================

Scientific quality metrics address the accuracy and reliability of our data products, and have been defined and tracked extensively throughout construction :cite:`LPM-17,DMTN-211,DMTN-091, LSE-63,DMTN-008, PSTN-023, SQR-008` and references therein. See :cite:`RTN-038` for a summary of how these quality metrics will be used in operations.

This document outlines the operational *non-quality* metrics for assessing and improving our system's performance and user experience. Non-quality metrics provide insights into the operational efficiency, usage patterns, infrastructure robustness, development processes, and security measures of the Data Management System. By monitoring these metrics, we aim to ensure that our infrastructure and services remain effective and secure, supporting our scientific objectives and user community.

Non-quality metrics are tracked by the various areas of oversight within DM.
Some examples of these metrics are as follows:

Data Production
---------------

**Software (Science Pipelines)**

- Deployment Frequency: *How often is* ``lsst_distrib`` *released?*
- Lead time for changes: *Average time to research, implement and changes of three different levels: *non-scientific-behavior bug fix,  scientific-behavior change, swapping in a new state of the art algorithm.*
- Average time to recovery: *time to notice and fix a breaking commit on main for both* ``lsst_distrib`` *itself and various conitnuous integration builds.*
- Average time to investigate an issue:

**Campaign Management (tracked jointly with Data Facility)**

These metrics are affected by infrastructure and also provide insights into the health of the storage, compute and networks.

- Peak number of cores used per workflow/campaign
- Wall time of a campaign
- CPU-time of a campaign
- Number of average concurrent cores used per workflow management system (e.g. htcondor, PanDA)

**Campaign Management (tracked jointly with Pipelines)**

These metrics are affected by the pipeline software and also provide insights into how to best configure pipeline algorithms for the available hardware.

- Core utilization efficiency (joint metric between pipelines and CM)
- Memory usage per workflow, task, and quanta

Data Services
-------------

The Science Platform metrics include:
  - Number of RSP accounts – total as a function of time
  - Active RSP accounts hour/day)


Data Facility Infrastructure
----------------------------


Metrics monitoring
==================

These metrics are monitored using:

- `Grafana <https://grafana.slac.stanford.edu>`__
- `Sasquatch <https://sasquatch.lsst.io/environments.html>`__
- `Human-reported logs on confluence <https://confluence.lsstcorp.org/display/DM/Average+time+to+recovery+for+pipelines+breakage>`__
- `Jenkins reporting tools <https://rubin-ci.slac.stanford.edu/job/scipipe/job/lsst_distrib/buildTimeTrend>`__


References
==========
.. bibliography::
