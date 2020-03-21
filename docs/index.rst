.. 2019-nCoV Data documentation master file, created by
   sphinx-quickstart on Sat Mar  7 16:44:25 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Argonne Data Repository
============================================

This repository is for sharing data used and/or produced by the project. Files are `located on the ALCF Petrel data store <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2F>`_, from where they can be retrieved via Globus (follow `this link <https://app.globus.org/groups/ebcae90a-60c9-11ea-a443-0a990c2810ad/about>`_ to request access permissions). Other files are `located on Argonne Box <https://anl.app.box.com/folder/105432421864>`_, but require Argonne credentials. There is also a read only copy of the Box data in ALCF Petrel data store, under the ``/BoxMirror/`` directory.

When using `Globus <https://app.globus.org>`_, these endpoint names may be useful:

* `2019-nCoV <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2F>`_: ALCF Petrel server, where the data listed below are to be found
* **anl#dtn_mira**: ALCF file systems, including Theta file system space at `/lus/theta-fs0/projects` (with 12 data transfer nodes [DTNs], better than endpoint **anl@theta**, which only has one)
* `anl#lambda0 <https://app.globus.org/file-manager?origin_id=8715e4f0-1d34-11ea-9705-021304b0cca7&origin_path=%2Flambda_stor%2Fdata%2F>`_: Argonne Lambda machine
* `anl#mllab <https://app.globus.org/file-manager?origin_id=2535d252-21ac-11e8-b75c-0ac6873fc732&origin_path=%2F~%2F>`_: Washington, Everett, nucleus

How do I upload data to the site?
---------------------------------

1. Upload the data to the ``/incoming/`` folder on the ALCF Petrel datastore (`here <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fincoming%2F>`_).
2. Post on the ``#data-incoming`` channel on Slack. *Make sure to provide a description of the data in a* ``README`` *or in the message you post to the slack.*
3. A data librarian will will move the data to a permanent place on the Globus endpoint and update the website with a link to the data and the description.

SMILEs that we are working with
-------------------------------


=========== ============= ====== ===========
Dataset     #SMILES       Size   Location(s)
=========== ============= ====== ===========
ChEMBL      1,870,462     103 MB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FChEMBL%2F>`_
DrugBank    9,679         664 KB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FDrugBank%2F>`_
eMolecule   22,318,616    830 MB version 2019-04-01 `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FeMolecules%2F>`_
ENAMIN_REAL >1.2B         32 GB  20 zip file `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FENAMIN_REAL%2F>`_ (`source <https://enamine.net/library-synthesis/real-compounds/real-database>`_), `deduplicated <https://app.globus.org/file-manager?destination_id=a386b552-6086-11ea-9688-0e56c063f437&destination_path=%2Fdatabases%2FENAMIN_REAL%2F>`_
GDB-13      977,468,301   2.7 GB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FGDB-13%2F>`_
GDB-17      50,000,000    1.5 GB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FGDB-17%2F>`_
HOPV15      350           27 KB  `Petrel <https://2019-ncov.e.globus.org/databases/HOPV15/smiles.txt>`_
Moses       1,936,963     81 MB  `Petrel <https://2019-ncov.e.globus.org/databases/Moses/dataset_v1.csv>`_
PubChem     97,584,282    925 MB pubcehm_canonical.tar.gz `Box <https://anl.app.box.com/file/631539842091>`_, `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fsmiles>`_
SureChEMBL* 291,525,153   35 GB  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FSureChEMBL%2F>`_
QM9         133,885       319 MB `Petrel <https://2019-ncov.e.globus.org/databases/QM9/dsgdb9nsd.xyz.tar>`_
REP         10,148        519 KB `Petrel <https://2019-ncov.e.globus.org/databases/REP/smiles.txt>`_
SAVI        283,194,319   989 GB `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FSAVI%2F>`_
ZINC        21,957,636    1.3 GB `Petrel <https://2019-ncov.e.globus.org/databases/ZINC/index.html>`_
ZINC15      1,475,876,222 92 GB  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FZINC15%2F>`_, `deduplicated <https://app.globus.org/file-manager?destination_id=a386b552-6086-11ea-9688-0e56c063f437&destination_path=%2Fdatabases%2FZINC15%2F>`_
ZINC15_3D   NA            NA     `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdatabases%2FZINC15_3D%2F>`_
=========== ============= ====== ===========

*Note: The SureChEMBL numbers are way off. In fact there are just 18M SMILEs, and not all are unique.

Computed descriptors
--------------------

============ ======== ============ ======== ============
enaDB        310,682  0.1GB                 `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fena15m_descriptors%2F>`_
ena15m       15M      116GB        1,555    `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fena15m_descriptors%2F>`_
pubchem      97M      726GB        9,755    `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2Fpubchem128_descriptors%2F>`_
Enamine_REAL >1.2B    8.55TB       120,694  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Fdescriptors%2FEnamine_Real_Descriptors%2F>`_
============ ======== ============ ======== ============

Note: "enaDB" is 310,682 ENA+Databank SMILES strings plus computed descriptors; 95 missing are `listed here <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2F>`_.

Toxicology
----------
============================================ =========== =========== ================================= =============
Dataset                                      Author      Size        Checksum                          Location(s)
============================================ =========== =========== ================================= =============
ena+db.can.uniq.csv.bsep.scaffold.class      Brettin     341.41MB    9d1441d895b43f7c7f8a740d4b2aedaf  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Ftoxicology%2F>`_
ena+db_tox21_screening.csv                   Ward        84MB        89c442d16415fa145a0fb4e112d323c7  `Petrel <https://app.globus.org/file-manager?origin_id=a386b552-6086-11ea-9688-0e56c063f437&origin_path=%2Fdata%2Ftoxicology%2Ftox21-screen-results%2F>`_
============================================ =========== =========== ================================= =============


ML Docking
-----------

Pending
