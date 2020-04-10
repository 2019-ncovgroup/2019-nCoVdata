The Polaris Collaboration Data Repository
=========================================

A Data Repository to Share AI- and HPC-enabled Generated for SARS-CoV-2 Drugs
-----------------------------------------------------------------------------

This repository is for sharing data and models used and/or produced by the Polaris collaboration. 
These data will be updated regularly as the collaboration produces new results.
Shared data are `located on the ALCF Petrel data store <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2F>`_, 
from where they can be retrieved via Globus (**to request access, follow** 
`this link <https://app.globus.org/groups/ebcae90a-60c9-11ea-a443-0a990c2810ad/about>`_). 


Data Processing Pipeline
=========================
The data processing pipeline is used to compute different types of features and representations of billions of small molecules. 
The pipeline first converts the SMILES representation for each molecule to the canonical SMILES form and removes duplicates. 
It then creates three different types of features: 1) molecular descriptors using `Mordred <https://github.com/mordred-descriptor/mordred>`; 
2) molecular fingerprints that encode the structure of molecules; and 3) 2D images of the molecular structure. 
These features are used as input to various machine learning and deep learning models that predict important
characteristics including docking scores, toxicity, and more.

.. image:: ./assets/pipeline.png
  :width: 800
  :alt: Data pipeline

Collected Datasets
===================
The following datasets have been collected and made available on Petrel for simplified access.
We are working on a combined database covering all molecules from these datasets.

=========== ============= ====== ===========
Dataset     #SMILES       Size   Location(s)
=========== ============= ====== ===========
ChEMBL      1,870,462     103 MB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FChEMBL%2F>`_
DrugBank    9,679         664 KB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FDrugBank%2F>`_
DUDE        101,337       6.9 MB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fsmiles%2FDUDE%2F>`_
eMolecule   22,318,616    830 MB  version 2019-04-01 `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FeMolecules%2F>`_
ENAMIN_REAL >1.2B         32 GB   20 zip file `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FENAMIN_REAL%2F>`_ (`source <https://enamine.net/library-synthesis/real-compounds/real-database>`_), `deduplicated <https://app.globus.org/file-manager?destination_id=a386b552-6086-11ea-9688-0e56c063f437&destination_path=%2Fdatabases%2FENAMIN_REAL%2F>`_
GDB-13      977,468,301   2.7 GB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FGDB-13%2F>`_
GDB-17      50,000,000    1.5 GB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FGDB-17%2F>`_
HOPV15      350           27 KB  `Petrel <https://2019-ncov.e.globus.org/databases/HOPV15/smiles.txt>`_
L1000       10148         603 KB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fsmiles%2FL1000%2F>`_
Moses       1,936,963     81 MB  `Petrel <https://2019-ncov.e.globus.org/databases/Moses/dataset_v1.csv>`_
PubChem     97,584,282    925 MB pubcehm_canonical.tar.gz `Box <https://anl.app.box.com/file/631539842091>`_, `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fsmiles>`_
QM9         133,885       319 MB `Petrel <https://2019-ncov.e.globus.org/databases/QM9/dsgdb9nsd.xyz.tar>`_
REP         10,148        519 KB `Petrel <https://2019-ncov.e.globus.org/databases/REP/smiles.txt>`_
SAVI        283,194,319   989 GB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FSAVI%2F>`_
SureChEMBL* 291,525,153   35 GB  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FSureChEMBL%2F>`_
ZINC        21,957,636    1.3 GB `Petrel <https://2019-ncov.e.globus.org/databases/ZINC/index.html>`_
ZINC15      1,475,876,222 92 GB  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FZINC15%2F>`_, `deduplicated <https://app.globus.org/file-manager?destination_id=a386b552-6086-11ea-9688-0e56c063f437&destination_path=%2Fdatabases%2FZINC15%2F>`_
ZINC15_3D   NA            NA     `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FZINC15_3D%2F>`_
=========== ============= ====== ===========

*Note: The SureChEMBL numbers are way off. In fact there are just 18M SMILEs, and not all are unique.

Computed descriptors
====================

============= ============= ======== ==========  ============
Dataset       #SMILES       Size      # Files     Location(s)
============= ============= ======== ==========  ============
DrugBank       9,679                              `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FDrunkBank_descriptors%2F>`_
DUDE           100k          6.9 MB               `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FDUDE_descriptors%2F>`_
eMolecule      22M           830 MB               `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FeMolecules_descriptors%2F>`_
Enamine_REAL   1.2B          8.55 TB  120,694     `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FEnamine_Real_Descriptors%2F>`_ (`manifest <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FEnamine_Real_Descriptors%2Fmanifest%2F>`_)
enaDB          310k          0.1 GB               `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fena15m_descriptors%2F>`_
ena15m         15M           116 GB   1,555       `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fena15m_descriptors%2F>`_ (`manifest <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fena15m_descriptors%2Fmanifest%2F>`_)
GDB-13         977M          7.24 TB  97,739      `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FGDB-13_descriptors%2F>`_
GDB-17         50M                                `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FGDB-17_descriptors%2F>`_
HOPV15         350                                `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FHOPV15_descriptors%2F>`_
L1000          10k                                `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FL1000_descriptors%2F>`_
Moses          1.9M                               `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FMoses_descriptors%2F>`_
PubChem        97M           726 GB   9,755       `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fpubchem128_descriptors%2F>`_
QM9            133k                               `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FQM9_descriptors%2F>`_
REP            10k                                `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FREP_descriptors%2F>`_
SAVI           283M                               `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fsavi_descriptors%2F>`_
SureChEMBL     291M          133 GB   1,792       `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FSureChEMBL_descriptors%2F>`_
ZINC           21M                                `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FZINC_descriptors%2F>`_
ZINC15         1.4B          11 TB    147,137     `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FZinc15_descriptors%2F>`_ (`manifest <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FZinc15_descriptors%2Fmanifest%2F>`_)
============= ============= ======== ==========  ============

Note: "enaDB" is 310,682 ENA+Databank SMILES strings plus computed descriptors; 95 missing are `listed here <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2F>`_.

Molecular Fingerprints
======================

============ =========
enaDB        TBA
ena15m       `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2FFingerprints%2FEnamine_REAL_diversity_set_15.5M%2F>`_
pubchem      `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2FFingerprints%2Fpubchem%2F>`_
Enamine_REAL TBA
ZINC15       TBA
SureChEMBL   `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2FFingerprints%2FSureChEMBL%2F>`_
============ =========

Molecular Images
======================

============ =========
TBA          TBA
TBA          TBA 
TBA          TBA
TBA          TBA 
TBA          TBA
TBA          TBA 
============ =========



Literature-Derived Screening Sets
=================================

Our researchers have assembled datasets of molecules to screen based on literature precedence. The molecules are extracted from literature manually
and matched to molecules in datasets by similarity search. The `.csv` files come in the following format: 
``Dataset_source, score, target_canonical_smile, match_canonical_smile``.

* `literature matches in the ENAMIN_REAL dataset <https://2019-ncov.e.globus.org/data/Top_Similar_Hits/top_100_similar_1000_targets/Enamine_Real_ben_literature_target_1000_targets_top_100_similar.top_100.csv>`_
* `literature matches in the GDB-13 dataset <https://2019-ncov.e.globus.org/data/Top_Similar_Hits/top_100_similar_1000_targets/GDB13_ben_literature_target_1000_targets_top_100_similar.top_100.csv>`_

A natural language processing model, trained to automate aspects of this process, will be made available in the future.


Toxicology
----------
Toxicology assessment is incorporated in the screening pipeline using a suite of machine learning models,
each trained on different datasets.
Details on the models and scripts to run them on new datasets are available `on GitHub <https://github.com/globus-labs/toxicity-prediction>`_

============================================  =========== ================================= =============
Dataset                                           Size        Checksum                       Location(s)
============================================  =========== ================================= =============
ena+db.can.uniq.csv.bsep.scaffold.class         341 MB    9d1441d895b43f7c7f8a740d4b2aedaf  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Ftoxicology%2F>`_
ena+db_tox21_screening.csv                      84 MB     89c442d16415fa145a0fb4e112d323c7  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Ftoxicology%2Ftox21-screen-results%2F>`_
Enamine_REAL_diversity_set_15M_tox21.csv        4.3 GB    3398960c27415eb27ec4ac577bdd906f  `Petrel <https://app.globus.org/file-manager?destination_id=a386b552-6086-11ea-9688-0e56c063f437&destination_path=%2Fdata%2Ftoxicology%2Ftox21-screen-results%2F>`_
============================================  =========== ================================= =============

Contributing Data
=================


1. Upload the data to the ``/incoming/`` folder on the ALCF Petrel datastore (`here <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fincoming%2F>`_).
2. Post on the ``#data-incoming`` channel on Slack. *Make sure to provide a description of the data in a* ``README`` *or in the message you post to the slack.*
3. A data librarian will move the data to a permanent place on the Globus endpoint and update the website with a link to the data and the description.


Pending
=======

ML Docking
----------
TBA


Top Docking Hits
----------------

We are currently working on hits for `vww`, `ADRP`, `ADRP-ADPR`, `CoV`, `Nsp10`, `nsp-15-CIT`, and `PLPro`. 
Results TBA


Top ML-Predictions
==================

The following table provides links to lists of drug candidates that our ML models 
score in the top 1% for several targets,and on what datasets the drugs come from. 
We have developed two primary models a binning model and a regressor model. The 
binning model XYZ, and the regressor model XYZ The `intersection` label are the drugs 
that scored in the top 1% under both binning models and the regressor models. 
(All links are to locations on Petrel)

 ====================== ============== ====================
 Target and Model       Dataset        Predictions by date
 3CLpro binner          ENAMIN_REAL    TBA
 3CLpro regressor       ENAMIN_REAL    TBA
 3CLpro intersection    ENAMIN_REAL    TBA
 ADRP-P1 binner         ENAMIN_REAL    TBA
 ADRP-P1 regressor      ENAMIN_REAL    TBA
 ADRP-P1 intersection   ENAMIN_REAL    TBA
 ====================== ============== ====================



Additional Data Access Details
==============================

Related Globus Endpoints
------------------------

When using `Globus <https://app.globus.org>`_, these endpoint names may be useful:

* `2019-nCoV <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2F>`_: ALCF Petrel server, where the data listed below are to be found
* `alcf#dtn_mira <https://app.globus.org/file-manager?origin_id=e09e65f5-6d04-11e5-ba46-22000b92c6ec>`_: ALCF file systems, including Theta file system space at `/lus/theta-fs0/projects` (with 12 data transfer nodes [DTNs], better than endpoint `alcf#dtn_theta <https://app.globus.org/file-manager?origin_id=08925f04-569f-11e7-bef8-22000b9a448b>`_, which only has one)
* `anl#lambda0 <https://app.globus.org/file-manager?origin_id=8715e4f0-1d34-11ea-9705-021304b0cca7&origin_path=%2Flambda_stor%2Fdata%2F>`_: Argonne Lambda machine
* `anl#mllab <https://app.globus.org/file-manager?origin_id=2535d252-21ac-11e8-b75c-0ac6873fc732&origin_path=%2F~%2F>`_: Washington, Everett, nucleus

`Get help setting up a Globus endpoint. <https://www.globus.org/globus-connect>`_


Data Access and Upload Via Box
------------------------------


*Argonne IT and cybersecurity have recently set up a Globus endpoint that interfaces
 directly with Box (i.e., data are replicated in both directions). 
 Using this capability will require you to have an Argonne login and access to the 2019 nCoV Box folder.
 * You can access it `here <https://app.globus.org/file-manager?origin_id=e0815163-39cf-4107-a8de-46310df195dc&origin_path=%2F>`_

Some files are `located on Argonne Box <https://anl.app.box.com/folder/105432421864>`_, 
but require Argonne credentials. There is also a read only copy of the Box data in ALCF Petrel 
data store, under the ``/BoxMirror/`` `directory <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2FBoxMirror%2F>`_, 
which is also replicated to ``/theta_projects/CVD_Research/BoxMirror`` on Theta.
These mirrors update approximately every hour from the data in Box.


Acknowledgements
==============================
Data storage and computational support for this research project has been generously supported by the following resources.

Petrel Data Service at the Argonne Leadership Computing Facility (ALCF)
-----------------------------------------------------------------------
This research used resources of the Argonne Leadership Computing
Facility, which is a DOE Office of Science User Facility supported under
Contract DE-AC02-06CH11357.
`Petrel <https://press3.mcs.anl.gov/petrel/>`_


Theta at the Argonne Leadership Computing Facility (ALCF)
---------------------------------------------------------
This research used resources of the Argonne Leadership Computing
Facility, which is a DOE Office of Science User Facility supported under
Contract DE-AC02-06CH11357.
`ALCF <https://www.alcf.anl.gov>`_


Frontera at the Texas Advanced Computing Center (TACC)
------------------------------------------------------
`TACC <https://www.tacc.utexas.edu>`_


Comet at the San Diego Supercomputing Center (SDSC)
---------------------------------------------------
`SDSC <https://www.sdsc.edu>`_


