# talking-data
Dataset for "The Relation between Developers’ Communication and Fix-Inducing Changes: An Empirical Study"

The dataset contains the following tree for each system folder:

<system>/
├── bts-data
├── chat-data
├── git-bts-integration-data
├── ml-data
└── networks_images

FILES INCLUDED:

*bugids.txt*       
------------
It is a list of bug identifiers, one per line, containing the processed bugs for bts system.

*bugs-metadata.csv*
------------------
This CSV files contains the following fields:
BUGID,ROLD-DATE,RFIX-DATE,FIXER,INDUCERS
For each bugid provides the date range under analysis (rold,rfix) , the FIXER
and the fix inducing committers.

*file-ownsers.csv*
------------------
This CSV file contains the commits in the considered range by committer and by file
used to evaluate ownership. It has the following fields:
BUGID: the bug identifier
_ROLDLESSNMONTSDATE_: the starting date (rold - 3 months)
_RFIXDATE_: the ending date (rfix)
_BUGFIXCHANGEDFILE_: one of the files changed by the fix
_COMMITTER_: the committer
_NUMOFCOMMITTSMADEONCHANGEDFILEBYCOMMITTERINTHEPERIOD_: the number of commits performed by the committer in the period

*<system>\_socialnetworks.zip*
------------------------------
Contains the networks constructed for the mailing lists source.
These are text files with the following header:
FROM|TO|DATE|FILES(;)
where
FROM and TO are the identifiers of the persons involved in the Communication
DATE is the date of the Communication
FILES are the files that are refereed in the text body separated by ;

*<system>-bts.zip*
------------------
Contains the networks constructed for the BTS source.
These are text files with the following header:
FROM|TO
where
FROM and TO are the identifiers of the persons involved in the BTS communication

*<network>.tar.gz*
------------------
Contains the networks constructed for the BTS source.
These are text files with the following header:
FROM|TO
where
FROM and TO are the identifiers of the persons involved in the chat communication

*network\_<system>\_<bugids>.eps*
----------------------------------
Several raster images of interesting networks.
