.. highlight:: rst

.. role:: strike
    :class: strike
	    
.. |br| raw:: html

   <br />

.. |nbsp| unicode:: 0xA0 
   :trim:
      
=====
Guide
=====

1. Data collection and documentation
====================================

1.1 What data will you collect, observe, generate or re-use?
------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    Questions you might want to consider:                                    
                                                                         
    * What type, format and volume of data will you collect, observe, generate or reuse?
    * Which existing data (yours or third-party) will you reuse?           

    Briefly describe the data you will collect, observe or generate. Also  
    mention any existing data that will be (re)used. The descriptions      
    should include the type, format and content of each dataset.           
    Furthermore, provide an estimation of the volume of the generated      
    datasets.                                                              
                                                                       
    (This relates to the FAIR Data Principles F2, I3, R1 & R1.2)

Instructions
^^^^^^^^^^^^
                                          
1. Identify each dataset
    (or collection of datasets that have the same
    characteristics with respect to content-type, source, format, etc.)
    and consider to introduce an abbreviation for each one.

2. For pre-existing datasets,
    briefly describe the content, role in the
    project, and the source.

3. For datasets to be produced in this project,
    briefly describe their
    content, role in the project, and how they will be collected,
    observed or generated.

4. For all datasets,
    mention the general data type (e.g., *text*,
    *tabular data*, *images*, *movies*, *audio files*, device-specific
    *binary data*, *geospatial data*, *census data*, ...) along with
    the their file-formats (as created by the device(s) used, by the
    simulation software, or as downloaded), e.g., ``CSV``,
    ``netCDF``, ``JPEG``, ``PNG``, ``MPEG-4``, ``PDF``,
    ``Shapefile``, ``VCF``, ``SMILES``, ... For datasets for which
    you have options to choose a file-format, please refer to
    :ref:`Appendix A: File format recommendations <file-formats>`.

5. For all datasets,
    give an estimate of the total volume and the number of files, if a
    large number of them is to be expected. Orders of magnitude are
    sufficient.

.. note::
   Make sure to not only consider the "raw" data, but also datasets that will be
   expected at the end of the analysis chain and directly underlie the
   resulting publications.

.. rst-class:: html-toggle

Example snippets
^^^^^^^^^^^^^^^^

Example 1 [UGLA2015-1]_
.......................

The data produced from this research project will fall into two          
categories:                                                              
                                                                             
1. The various reaction parameters required for optimization of the chemical transformation.
2. The spectroscopic and general characterization data of all compounds produced during the work.

All data is tabular. Data in category 1 will be documented in [*file_format*].
Spectroscopic data in category 2 will be produced as [*file_format*]   
and converted to [*file format*] for further use. Other 
characterization data in this category will be collected in [*file_format*].

We anticipate that the data produced in category 1 will amount to
approximately 10 MB and the data produced in category 2 will be in
the range of 4 - 5 GB.

Example 2 [UGLA2015-2]_
.......................
	    
This project will work with and generate four main types of raw data:

1. Images from transmitted-light microscopy of giemsa-stained squashed larval brains.
2. Images from confocal microscopy of immunostained whole-mounted larval brains.
3. Western blot data.
4. Results from LC/MS analyses of larval brains 

All data will be stored either in the format in which it was
originally generated (i.e. Metamorph files for confocal images;
Spectrum Mill files for mass spectra with results of mass spectra
analyses stored in CSV files; TIFF files for transmitted-light
microscopy), or will be converted into a digital form via scanning
to create TIFF or JPEG files (e.g. western blots or other types of
results).
    
Measurements and quantification of the images will be recorded in
Excel files. For long term preservation, they will be converted to
CSV files. Micrograph data is expected to total between 100 GB and
1 TB over the course of the project. Scanned images of western
blots are expected to total around 1GB over the course of the
project. Other derived data (measurements and quantification) are
not expected to exceed 10 MB.

Example 3 (modified from [EPFL2017]_)
.....................................
	    
The data are tabular health records generated by users of the
application X, which is deployed to 2 million users by company Y,
who will also collect the data from all users to provide us with
the complete dataset.

All fields contain user observations and are entered manually,
except for temperature, which is measured by a Bluetooth connected
thermometer. Data recording will take place over the course of three months.

Data fields per user: User identifier, Age, Weight, Size.

Six data fields per users per day of observation, which include one
numerical value (temperature), five values on a nominal scale,
e.g. "cervical fluid quality", and one free-text field.

Data will be received in CSV format and has a total volume of about 15 GB.

Example 4 (from real Eawag DMP)
...............................

There will be two categories of data: NEW data from this project and
EXISTING data from the FOEN Lake Monitoring program. The NEW data will
consist of several file types, all CSV real number format, which are
all organized along the same principle: matrixes of times series with
various channels, each corresponding to a sensor (number of sensors
varies from 1 to10) and very different length, as the sampling
frequency varies by several orders-of-magnitudes. (i) 6 files of CO2,
DO, PAR and temperature (24 files at a time; Figure 2), each file only
1 sensor (Delta = 10 min; continuous), (ii) Thetis profiles
corresponding to time series (equivalent to depth series) of 10
sensors (Delta = 1 s; 5-10 times per day). (iii) 5 files of CO2 time
series for short-term surface flux measurements (several files, one
per month), (iv) meteodata file (eight sensors; continuous), (v)
T-Microstructure profiles files (6 sensors at 512 Hz; several files,
once per month) and (vi) excel files for individual chemical samples
(such as alkalinity, sediment trap estimates, ect; sporadic). The
EXISTING data is already available (CIPAIS, CIPEL) in excel sheets
with matrices for the individual samplings and a variable number of
parameters (~10 to ~25). The EXISTING data will not be modified and
remains with the organizations. We will keep a copy on our computers
during the project.  We anticipate the data produced in category 1 to
amount to several hundred MB for the moored and profiled sensor files
and ~100 GB for the T-microstructure profiles; the EXISTING data in
category 2 is in the range of ~20 MB.

1.2 How will the data be collected, observed or generated?
----------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    Questions you might want to consider:                                    
                                                                         
    * What standards, methodologies or quality assurance processes will you use? 
    * How will you organize your files and handle versioning?

    Explain how the data will be collected, observed or generated.
    Describe how you plan to control and document the consistency and
    quality of the collected data: calibration processes, repeated
    measurements, data recording standards, usage of controlled
    vocabularies, data entry validation, data peer review, etc.
                                                                         
    Discuss how the data management will be handled during the project,  
    mentioning for example naming conventions, version control and folder
    structures. (This relates to the FAIR Data Principle R1)             

Instructions
^^^^^^^^^^^^

This section actually has two parts, **1. Quality Control** and **2. Organization**.

1. Quality assurance
....................   
	    
For each dataset, mention standards, methodologies and processes that
serve to ensure that the data meets the expected quality. This
might for example include:

* The use of core facility services (specify their certifications, if any)
* Codes of good research practice that are being followed.
* Quality control procedures such as plausibility checks, range check,
  double data entry, statistical or visual outlier detection,
  instrument verification tests, etc., that you
  plan to apply.
* The method to record data quality (e.g. quality flags for data
  points), if applicable.
* Arrangements to assign responsibilities for quality control.
* Training activities.

    
2. Data Organization
....................

Briefly describe how the data will be organized. That might be a
folder-structure together with a file naming convention, a local SQL
or NoSQL database, a cloud-based collaboration platform, a
version-control system such as git, an Electronic LaboratoryNotebook /
Laboratory Information System (ELN/LIMS), etc.

Consider how the chosen organization schema supports version-control
(if necessary), collaboration (if necessary) and is suited for the
expected data volume and data structure.

.. rst-class:: html-toggle
	       
Example snippets
^^^^^^^^^^^^^^^^

Example 1 (modified from [UGLA2015-1]_)
.......................................

The reaction conditions will be recorded and collated using a
spreadsheet application. The resulting files will be saved in
directory, one for each scientist, with appropriately set file
permissions. A filename convention that encodes reaction, reaction
generation and date will be applied.

These directories will be mirrored to SWITCHDrive to for collaboration.
                                                                        
The various experimental procedures and associated compound             
characterization will be written up using the Royal Society of Chemistry	    
standard formatting in a Word document, each Word document will also be 
exported to PDF-A. The associated NMR spectra will be collated in       	    
chronological order in a PDF-A document.                                

Example 2 (modified from [UGLA2015-2]_)
.......................................
                                                                        
All samples on which data are collected will be prepared according to
published standard protocols in the field \[*cite reference*\]. Files
will be named according to a pre-agreed convention. The dataset will
be accompanied by a README file which will describe the directory
hierarchy. Each directory will contain an INFO.txt file
describing the experimental protocol used in that experiment. It
will also record any deviations from the protocol and other useful
contextual information.

The format used for microscope images captures and stores a range of
metadata (field size, magnification, lens phase, ...) with each
image. We will use a Python script that automatically extracts these
metadata and stores them together with the respective filenames in a
SQLite database.

Example 3 (from a real Eawag DMP)
.................................

The data from the moored sensors is sensor-internally stored and
recovered every two months, when sensors will be cleaned and
recalibrated if data indicates quality loss. The CO2 sensors will be
cross calibrated against atmospheric pressure. The DO and PAR sensors
in the mooring will be compared to profiled sensors and deviations
detected. Temperature sensors are extremely stable and are only
calibrated before and after the two years using the laboratory
temperature bath which is calibrated agaist the Office of Metrology in
Bern every few years to 0.001 oC.  The Thesis sensor data is
transmitted when surfacing via GSM communication system directly to
the lab where sensors deterioration is weekly checked. The instrument
will be retrieved every month and sensors cleaned. The optical sensors
will be calibrated according the manual every six months. The
T-microstructure sensors do not need calibration as the data is
matched to (very accurate) CTD temperature. Small T shifts are
irreverent, as only the spectra matter. The sensors deterioration (or
frequency loss) will visually be checked and is seen in the quality of
the Batchelor spectra.  The very simple structure of the CSV files
holding the raw data will be documented in a plain text README
file. This file, and all raw data files as they become available, will
be uploaded to the Eawag Research Data Institutional Collection into
one “data package”, which is annotated with general metadata.  Copies
of the raw data files as well as set of calibrated, quality-controlled
files stored on the group computers at EPFL will be organized in a
folder structure that is also documented in a README file. At the end
of the project, the entire set of calibrated, quality-controlled files
will be annotated and stored on the Eawag institutional repository as
well.

Example 4 [EPFL2017]_
.....................
	    
All experimental data will be automatically imported into the
institutional electronic Laboratory Information System (LIMS) from the
measurement device. Methods and materials will be recorded using the
institutional Electronic Lab Notebook (ELN).

Example 5
.........

The sensor data are being fed into a Postgresql database running on an
institutional server. The database implements rules for basic validity
checks (range-checks, plausibility checks). The R scripts for data
analysis are stored in the institutional Git repository for version
control and collaboration.


1.3 What documentation and metadata will you provide with the data?
-------------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
   
    Questions you might want to consider:
    
    * What information is required for users (computer or human) to
      read and interpret the data in the future?
    * How will you generate this documentation?
    * What community standards (if any) will be used to annotate the (meta)data?
      
    Describe all types of documentation (README files, metadata, etc.)
    you will provide to help secondary users to understand and reuse
    your data. Metadata should at least include basic details allowing
    other users (computer or human) to find the data. This includes at
    least a name and a persistent identifier for each file, the name
    of the person who collected or contributed to the data, the date
    of collection and the conditions to access the data.
    
    Furthermore, the documentation may include details on the
    methodology used, information about the performed processing and
    analytical steps, variable definitions, references to vocabularies
    used, as well as units of measurement. Wherever possible, the
    documentation should follow existing community standards and
    guidelines. Explain how you will prepare and share this
    information. (This relates to the FAIR Data Principles I1, I2, I3,
    R1, R1.2 & R1.3)

Instructions
^^^^^^^^^^^^

Conceptualize two types of metadata: **1. Scientific metadata** and
**2.  General metadata**:

1. Scientific metadata
......................   

Scientific metadata provides all necessary information to correctly
understand, interpret, assess, replicate (within limits), build upon,
and generally use your data. This metadata might be compiled
"free-form" into one or several README-file(s) that accompany the
data.

Certain fields have formally defined established metadata standards,
e.g. the `Ecological Metadata Language (EML)
<https://knb.ecoinformatics.org/#external//emlparser/docs/index.html>`_,
the `Open Microscopy Environment Schemas
<https://docs.openmicroscopy.org/ome-model/5.5.7/index.html>`_ or
`WaterML <http://www.opengeospatial.org/standards/waterml>`_. Mention
it, if you use such a standard. Have a look at `The RDA metadata
directory
<http://rd-alliance.github.io/metadata-directory/standards/>`_ for an
overview of existing standards.

This metadata could contain for example:

* A description of the organization and relationships of the files or
  database tables and other supporting materials.
* Information about the naming convention (if applicable).
* A mapping of data files to the corresponding section of the
  associated publication, if applicable.
* Information about units of measurements, variable definitions,
  columns headings and abbreviations (if not present in the data-files
  proper).
* Information about the software (name, version, system environment).
  used to produce and read the data (if the software is not included
  as data).
* Information about which files were used in what way at what stage of
  the work.
* Suggestions for how to best reuse the data.
* Any information suited to decrease the chances that a future user of
  the data needs to contact you with questions.

**Describe, as detailed as possible, what will comprise the scientific
metadata.**  Make sure to mention all information, or information
categories, that a future user of your data will need to read and
interpret the data.

**Describe how this metadata will be managed,** i.e. who or what will
generate it when, in what form it is stored in which location, and how
it is associated with the respective experiment, measurement, or
observation. Describe technical aspects of the metadata management,
e.g. the use of database software, and the protocol or mechanism to
handle updates and version control, if applicable.

2. General metadata
...................

This type of metadata serves to make your data findable. It consists
of general attributes that help to search, sort, index, access and
propagate the dataset or collection of datasets. At Eawag, capture,
storage, formatting and dissemination of this metadata is handled by
the `institutional research data repository
<https://eaw-ckan-dev1.eawag.wroot.emp-eaw.ch/>`_. You might use the
:ref:`Eawag standard snippet "metadata in ERIC"
<eawag_standard_eric1>`.


.. rst-class:: html-toggle
	       
Examples for 1. Scientific metadata
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Example 1 [DataONE2011]_
........................

We will first document our metadata by taking careful notes in the
laboratory notebook that refer to specific data files and describe all
columns, units, abbreviations, and missing value identifiers.  These
notes will be transcribed into a .txt document that will be stored
with the data file. After all of the data are collected, we will then
use EML (Ecological Metadata Language) to digitize our metadata. EML
is one of the accepted formats used in ecology, and works well for the
types of data we will be producing.  We will create these metadata
using Morpho software, available through KNB
(http://knb.ecoinformatics.org/morphoportal.jsp). The metadata will
fully describe the data files and the context of the measurements.


Example 2 [UGLA2015-1]_
.......................

The data will be accompanied by the following contextual documentation, according to
standard practice for synthetic methodology projects:

1. spreadsheet documents which detail the reaction conditions. 
2. text files which detail the experimental procedures and compound characterization.
   
Files and folders will be named according to a pre-agreed convention. 
The final dataset as deposited in the institutional data repository will also be
accompanied by a README file listing the contents of the other files and outlining the
file-naming convention used.

Example 3 (from a real Eawag DMP)
.................................
	    
For every data stream (sequences of identical data files) over the
entire 2-year period of data acquisition a README File will be
generated which contains: (a) the sensors used (product, type, serial
number), (b) the temporal sequence of the sensors (time and location,
sampling interval), (c) the observations made during maintenance and
repairs, and (d) details on the physical units, as well as the
calibration procedure and format. This is a standard procedure which
we have used in the past.

	       
Example for 2. General metadata
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. _eawag_standard_eric1:

.. admonition:: Eawag standard snippet "metadata in ERIC"
    :class: admonition-eawag-standard-snippet
	    
    The completed dataset will be uploaded to the Eawag Research Data
    Institutional Collection (ERIC). This repository collects (upon
    upload) the metadata according to the `DataCite metadata schema
    4.0 <http://doi.org/10.5438/0012>`_, an accepted state-of-the-art
    standard. In addition to the mandatory fields of the DataCite
    schema, ERIC collects several metadata fields such as
    *time-range*, *spatial extent*, *geographical names*, *measured
    variables*, *chemical substances* and taxonomic information. ERIC
    provides search functionality and assigns a persistent URL to each
    dataset.

2. Ethics, legal and security issues
====================================

.. _section2.1:

2.1 How will ethical issues be addressed and handled?
-----------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    Questions you might want to consider:                                    
                                                                                
    * What is the relevant protection standard for your data? Are you
      bound by a confidentiality agreement?
    * Do you have the necessary permission to obtain, process,
      preserve and share the data? Have the people whose data you are
      using been informed or did they give their consent?
    * What methods will you use to ensure the protection of personal
      or other sensitive data?
       
    Ethical issues in research projects demand for an adaptation of
    research data management practices, e.g. how data is stored, who
    can access/reuse the data and how long the data is stored. Methods
    to manage ethical concerns may include: anonymization of data;
    gain approval by ethics committees; formal consent agreements. You
    should outline that all ethical issues in your project have been
    identified, including the corresponding measures in data
    management. (This relates to the FAIR Data Principle A1)

Instructions
^^^^^^^^^^^^

1. Make sure you have a good idea what *personal data* means in the context of Swiss data protection law:
   *Personal data* refers to any information that relates to a particular
   person. Next to items such as physical- or email-address, health
   record, or age, it also includes for example photographs, videos
   recordings or genetic information. If in doubt, consult the `Eawag
   Compliance Guide (page 18)
   <https://www.internal.eawag.ch/en/legal-basis/directives-internal-regulations/compliance-guide/>`_
   and references therein.
   
2. Check whether your project involves the collection, storage or processing of *personal data*.

3. Check whether your project involves other types of sensitive
   information, e.g. otherwise not easily obtainable information about
   vulnerabilities of water infrastructure or locations of rare and
   protected species.

4. Check whether your work involves data that you obtain under a
   non-disclosure agreement or any kind of contract that would restrict
   its usage or dissemination, or includes other special requirements
   relevant for data handling.

5. If your project requires the assessment of an ethical review board (or
   similar), or requires permission from third parties such as a
   cantonal office, check whether any imposed requirements are related
   to data collection, processing or dissemination.

If the your project is free from any of the above issues, you might
copy & paste :ref:`Eawag standard snippet "no issues" <no_issues>`.

Otherwise:|br|
Specify all data that are affected by any of the above points. Specify
the special requirements regarding data collection, handling and
dissemination. 

The collection of personal data most likely requires informed
consent. Describe consent-form content and ancillary measures to
ensure informedness, if applicable.

Mention relevant approvals and permissions obtained from third parties
and reference their requirements.

If you anonymize personal data, describe the anonymization method
(e.g. pseudonymization or removal of personal information).

If you use encryption and/or if you put in place special access
restrictions, just mention that here and refer to :ref:`Section 2.2
<section2.2>`, where you give the details.

Mention non-technical procedures that ensure data protection, such as
scheduled deletion of data or training activities. For technical
implementation details or purely technical measures reference
:ref:`Section 2.2 <section2.2>`.

.. _no_issues:

.. admonition:: Eawag standard snippet "no issues"
   :class: admonition-eawag-standard-snippet

   There are no ethical, legal or security issues regarding data
   collection, processing, storage and dissemination in this
   project. We neither obtain nor generate sensitive data and do not
   sign a confidentiality agreement.
   
.. rst-class:: html-toggle
		    
Examples
^^^^^^^^
    
Example 1
.........

Dataset X was obtained from the BAFU and is subject to a
confidentiality agreement to keep information about the sampling
locations secret. We are allowed to share this information among
researchers involved in the project. The dataset is being stored in a
location to which only project member have access. Please refer to
:ref:`Section 2.2 <section2.2>` for technical details about access
restrictions. All project members will be informed about sensitivity
of this data and agree not to copy it to other places. This dataset
and intermediate datasets containing the sampling locations will be
excluded from the data package published along with the final report
and replaced with instructions about how to obtain them from the BAFU.

Example 2 [ESRC2013]_
.....................
	    
A letter explaining the purpose, approach and dissemination strategy
(including plans to share data) of the research, and an accompanying
consent form (including to share data) will be prepared and translated
into the relevant languages. A clear verbal explanation will also be
provided to each interviewee and focus group participant. Commitments
to ensure confidentiality will be maintained by ensuring recordings
are not shared; that transcripts are anonymized and details that can
be used to identify participants are removed from transcripts or
concealed in write-ups. Please refer to :ref:`Section 2.2 <section2.2>` for
technical details regarding anonymization method and techincal
measures.

Example 3
.........

The raw data from our metabolite measurements could, in concert with
other data, potentially be used to associate individual households
with drug-use profiles. We therefore regard the sampling locations as
sensitive data. In all published data, the sampling locations will be
replaced with numerical codes. The respective correspondence table
will be stored encrypted, please refer to :ref:`Section 2.2
<section2.2>` for technical details.

.. _section2.2:
    
2.2 How will data access and security be managed?
-------------------------------------------------

.. admonition:: SNSF [SNSF2017]_

    Questions  you might want to consider:

    * What are the main concerns regarding data security, what are the
      levels of risk and what measures are in place to handle security
      risks?

    * How will you regulate data access rights/permissions to ensure the
      security of the data?

    * How will personal or other sensitive data be handled to ensure safe
      data storage and transfer?

    If you work with personal or other sensitive data you should outline
    the security measures in order to protect the data. Please list formal
    standards which will be adopted in your study. An example is ISO
    27001 - Information security management. Furthermore, describe the
    main processes or facilities for storage and processing of personal or
    other sensitive data. (This relates to the FAIR Data Principle A1)


Instructions
^^^^^^^^^^^^

Briefly mention the datasets that require special protection
(reference :ref:`Section 2.1 <section2.1>`) and use an adverb to
indicate the "level of risk" (e.g. "high", "medium", "low").

To document proper handling of sensitive data consider the following
points and recommendations:

1. Storage location(s)
    Do not store sensitive data "in the cloud", unless the service
    provider is bound by Swiss privacy law. If you have to, encrypt it
    (see :ref:`Note on encryption <note_on_encryption>`). Mention any
    considerations in that regard, if applicable.

2. Secure transmission
    Encrypt sensitive data before transmission over a network and
    mention it if you do that. Public key encryption is the
    recommended method (see :ref:`Note on encryption
    <note_on_encryption>`).

3. Access restrictions
    Describe who has access to the data at what stage and how you
    implement access restrictions (e.g. by permissions on the file system).

4. IT Infrastructure
    Describe the IT infrastructure used with regard to data
    security. You might use :ref:`Eawag standard snippet "Eawag file
    services - access" <eawag_fileservices_access>`, if applicable.
    
.. _note_on_encryption:
   
.. admonition:: Note on encryption
    :class: admonition note alert alert-info
	    
    Consider encrypting sensitive information. In that case, name the
    encryption method, at what stage the data is encrypted, and how
    the encryption key is managed. In particular, consider using
    full-disk encryption for field notebooks, and public-key
    encryption for exchanging sensitive information (e.g. in emails or
    email-attachments, or when using untrusted file-sharing services
    such as Dropbox. `GnuPG <https://gnupg.org/index.html>`_
    is the recommended software for that purpose.

.. _eawag_fileservices_access:
.. admonition:: Eawag standard snippet "Eawag file services - access"
    :class: admonition-eawag-standard-snippet		

    All data will be stored on Eawag's central shared Fileservices. Data
    security and confidentiality are protected by using Microsoft Active
    Directory authentication. The shared filesystem can only be accessed
    from inside the Eawag network and remote access is possible by
    establishing a Virtual Private Network (VPN) that is secured by
    2-factor authentication.

.. rst-class:: html-toggle

Examples
^^^^^^^^

Example 1 [Leeds2013]_
......................
	    
Access to electronic data is controlled by Active Directory (AD) Group
membership. The Faculty IT Manager will set up a dedicated folder for
this research project and create read-only and read-write AD
groups. The PI will decide which users require read-only and
read-write access. Off-campus access is via the Citrix portal.
External users who need access to the data will apply for a University
username and then be assigned to the appropriate AD group.

Example 2 (modified from [NEH2015]_)
....................................

Research records will be kept confidential, and access will be limited
to the PI, primary research team members, and project
participants. Data will be housed on a local server controlled by the
PI, and will be accessible via SSH and VPN. Data containing
identifiable information, or information covered by an NDA, will be
held in an encrypted format (symmetric, AES256, key on local server,
passphrase only know to PI and primary research team members).

Example 3 (from a real Eawag DMP)
.................................

The data we are generating, processing and storing in this project
does not pose a particular data security risk. Day-to-day work is
conducted on standard-issue workstations in the EPFL-environment with
standard enterprise-grade access control. The EPFL network is a
secured system following the best practices in terms of identity
management and central storage facility has redundancy, mirroring and
is monitored. At different stages, data will be stored in the Eawag
Institutional Collection (see section 1.3). This system is accessible
only from within the Eawag network and is comprised of several
virtualized Linux systems that receive real-time security
patches. Access control is handled according to recognized best
practices of server administration.

2.3 How will you handle copyright and Intellectual Property Rights issues?
--------------------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    Questions you might want to consider:

    * Who will be the owner of the data?
    * Which licenses will be applied to the data?
    * What restrictions apply to the reuse of third-party data?

    Outline the owners of the copyright and Intellectual Property
    Right (IPR) of all data that will be collected and generated,
    including the licence(s). For consortia, an IPR ownership
    agreement might be necessary. You should comply with relevant
    funder, institutional, departmental or group policies on copyright
    or IPR. Furthermore, clarify what permissions are required should
    third-party data be re-used. (This relates to the FAIR Data
    Principles I3 & R1.1)

Instructions
^^^^^^^^^^^^^

1. If your work involves data that you obtain under a non-disclosure
   agreement or any kind of contract that would restrict its usage or
   dissemination (see :ref:`Section 2.1 <section2.1>`), consider how that
   impacts your right to disseminate derived data and your
   results and elaborate.

2. In case your data or source code might be commercially exploitable
   (e.g. patentable), please consult the `Technology Transfer Office at
   Empa <https://www.empa.ch/web/s607/technologietransfer>`_.

3. Results from work of Eawag employees is
   generally "owned" by Eawag. If your project involves groups from
   other institutions, make sure that there is an agreement about a
   common policy on the dissemination of results. Mention such an
   agreement or state that Eawag has the sole authority to
   disseminate the data.

4. After having established who owns / will own the rights on all
   data, software and other creative works that will be produced or
   used in or by the project, consider the :ref:`Note on licenses
   <note_on_licenses>` below. If you can release all relevant data,
   software and other creative works relevant for the project into the
   public domain, you might use the :ref:`Eawag standard snippet
   "default licensing" <eawag_standard_licenses>` and move on.


5. Otherwise state for all data, source code and other output under
   what terms it will be made available at the end of the project, and
   why it can't be released into the public domain, if applicable. If
   parts of the output or pre-existing data can not be made available
   at all, state that here and give the reason.

   If the reasons for not releasing the data, or releasing it under
   terms that restrict re-use, are related to the presence of
   "sensitive data" in the sense of :ref:`Section 2.1 <section2.1>`,
   reference :ref:`Section 4.2 <section4.2>`, where you explain the
   details.


.. _note_on_licenses:

.. admonition:: Note on licenses
    :class: admonition note alert alert-info

    \1. Pure data,
     "facts about nature", are not subject to
     copyright law in Switzerland. However, to make clear to potential
     users that they can re-use it, explicitly place it in the public
     domain by applying the `CC0 Public Domain Dedication
     <https://creativecommons.org/publicdomain/zero/1.0/>`_.
     
    \2. Source code
     falls *sui generis* under copyright law and you need to
     explicitly waive the copyright to enable unrestricted
     re-use. Apply the `CC0 - Public Domain Dedication
     <https://creativecommons.org/publicdomain/zero/1.0/>`_.

     If you want to have the option to sue people who don't credit you
     when using your code, apply the `MIT License
     <https://opensource.org/licenses/MIT>`_.

     If you like to force people who build on your code to open source
     their changes and improvements as well, apply the `GNU Affero
     General Public License
     <https://opensource.org/licenses/AGPL-3.0>`_.

     If your code builds on third-party code, check whether the
     respective license restricts your choice of license (e.g., if you
     build on code licensed under the GNU General Public License, GPL,
     you need to publish your derived code under a compatible license,
     or not publish it at all). If you have trouble to sort out your
     license-entanglements, get in touch with the `Eawag Research Data
     Management Project \<rdm@eawag.ch\> <rdm@eawag.ch>`_ for help.

    \3. Other creative output
     such as text, images, video also falls *sui generis* under
     copyright law and you need to explicitly waive the copyright to
     enable unrestricted re-use. Apply the `CC0 Public Domain
     Dedication <https://creativecommons.org/publicdomain/zero/1.0/>`_.

     If you want to have the option to sue people who don't credit you
     when re-using your work, apply the `Ceative Commons Attribution
     4.0 International License
     <https://creativecommons.org/licenses/by/4.0/>`_.
     
     In case you derived such a work from a pre-existing source, check
     whether restrictions imposed by the license of the original exist
     and publish your derivative work under a compatible license, if
     possible.
		   
.. _eawag_standard_licenses:
.. admonition:: Eawag standard snippet "default licensing"
    :class: admonition-eawag-standard-snippet		

    All software, datasets and other creative works from this project
    will be placed in the public domain by applying the Creative
    Commons Public Domain Dedication (CC0 1.0). Eawag has either
    unrestricted authority over the dissemination of the data and
    works to be published, or we have established an agreement to that
    effect with our collaborators.

.. rst-class:: html-toggle
	    
Examples
^^^^^^^^

Example 1
.........
	    
The source code for analysis will most likely utilize the GNU
Scientific Library (GSL), which is licensed under the GNU General
Public License (GPL). Therefore we will make our analysis software
available under the GPL as well.

Example 2
.........

Our collaborators at X University in Germany will contribute
significantly to produce the extensive database of species
distributions, which, in Germany, falls under copyright law. University
X would like to retain the copyright on the database and therefore it
will be published without a license that could facilitate re-use.

Example 3 (modified from [EPFL2017]_)
.....................................

This project is being carried out in collaboration with an industrial
partner. The intellectual property rights are set out in the
collaboration agreement. The intellectual property generated from this
project will be fully exploited with help from the institutional
Technology Transfer Office. The aim is to patent the final procedure
and then publish the work in a research journal and to publish the
supporting data under the Creative Commons
Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND
4.0) license.

3. Data storage and preservation
================================

3.1 How will your data be stored and backed-up during the research?
-------------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_

    Questions you might want to consider:

    * What are [*sic*] your storage capacity and where will the data be stored?
    * What are the back-up procedures?

    Please mention what the needs are in terms of data storage and
    where the data will be stored. Please consider that data storage on
    laptops or hard drives, for example, is risky. Storage through IT
    teams is safer. If external services are asked for, it is important
    that this does not conflict with the policy of each entity involved in
    the project, especially concerning the issue of sensitive
    data. Please specify your back-up procedure (frequency of updates,
    responsibilities, automatic/manual process, security measures, etc.)

Instructions
^^^^^^^^^^^^

Describe storage location and backup procedure during all phases of research, e.g.
a), during data collection / generation, and b), during analysis.

1. At stages where data can not be stored on Eawag infrastructure
   (e.g. fieled campaign involving dataloggers and laptops), take care
   to implement a backup protocol that should
   
   * be as automatic as possible,
   * frequent enough,
   * duplicate the data onto another storage medium, which
   * is kept at a different location and
   * ideally includes (automatic) checks for the success of each backup.

   From copying data from the field-laptop to a flash drive that is
   kept by another person to automatic synchronization with
   SWITCHDrive, there are many options to do this reliably and
   comfortably. Consult your IT department if you need help, or just to
   assess you strategy. Describe this backup strategy.

2. At a stage where you have access to the Eawag shared filesystem,
   store your data there. Make sure you know which directories of your
   workstation are mapped to backed-up server storage (see `IT
   documentation - Backup
   <https://www.internal.eawag.ch/en/it-services/data-management/backup/>`_). Check
   with IT whether you have access to the required storage capacity
   and arrange an increase of the quota, if necessary. Copy & paste
   the text-snippet below (:ref:`Eawag standard snippet "file
   services - backup" <eawag_file_services>`) to account for this
   stage.

3. In case you plan to use other servers, e.g. for doing bioinformatics
   at the Genetic Diversity Centre, inquire about their backup
   procedure and briefly describe it here. In case you need to set up a
   backup-solution by yourself, consider getting advice from the IT
   department.

4. In case you plan to use cloud storage for collaboration
   (e.g. SWITCHDrive), make sure a replica of that data is kept on
   Eawag infrastructure at any time. Encrypt sensitive that is being
   stored by third parties. Mention such a setup here.

5. Check whether you have the necessary storage capacity at all
   storage locations you plan to use. Mention that here (if not
   already covered by :ref:`Eawag standard snippet "file services -
   backup" <eawag_file_services>`.

.. _eawag_file_services:
   
.. admonition:: Eawag standard snippet "file services - backup"
    :class: admonition-eawag-standard-snippet	

    Data will be stored on back-upped servers in the Eawag local
    network. For file services and virtual server farm, Eawag shares a
    server/storage platform (Netapp Metrocluster, Cisco UCS Server,
    VMWare) with Empa. The backup procedure is fully automatic. Snapshots
    of files are taken at least three times during a working day. All data
    are mirrored synchronously between the two server sites on the
    Empa-Eawag campus in Dübendorf. Additionally, backups (to disk) are
    taken from the Metrocluster at a third location on the campus. Backups
    are kept for three months. We have arranged to have access to the
    required storage-capacity.

.. rst-class:: html-toggle

Examples
^^^^^^^^

Example 1
.........

Data will be downloaded from the dataloggers diurnally to the
field-laptop, and immediately copied to a flash-drive, which is stored
in a physically secure location in the field office. Success of the
download is checked immediately. The laptop is brought to Dübendorf
campus (no network link on-site) on the same day and the data is
copied to a backed-up server in the Eawag local network. [copy text
from :ref:`Eawag standard snippet "file services - backup"
<eawag_file_services>`]

Example 2
.........

The simulations will be carried at supercomputing facility X, where
backup is not available. On the local workstation runs a script that
periodically calls :code:`rsync` to mirror the remote directory, where
the simulation results are written, to a backed-up share on Eawag
infrastructure (which is mounted on the local workstation). [copy text
from :ref:`Eawag standard snippet "file services - backup"
<eawag_file_services>`]

Example 3
.........

Our team stores the data to be analyzed along with the results using
Eawag file services. [copy text from :ref:`Eawag standard snippet
"file services - backup" <eawag_file_services>`] To easily share data
with our collaborators in Fribourg, we synchronize those data with a
folder on SWITCHdrive. Since this is sensitive personal data, the
folder being synchronized contains encrypted files (public key
encryption, key-pairs specifically created for this project).

3.2 What is your data preservation plan?
----------------------------------------

.. admonition:: SNSF [SNSF2017]_

    Questions you might want to consider:

    * What procedures would be used to select data to be preserved?
    * What file formats will be used for preservation?

    Please specify which data will be retained, shared and archived
    after the completion of the project and the corresponding data
    selection procedure (e.g. long-term value, potential value for
    reuse, obligations to destroy some data, etc.). Please outline a
    long-term preservation plan for the datasets beyond the lifetime
    of the project. In particular, comment on the choice of file
    formats and the use of community standards. (This relates to the
    FAIR Data Principles F2 & R1.3)

Instructions
^^^^^^^^^^^^

It is Eawag policy to generally preserve *all relevant data* generated
or used by research projects in the `Eawag Research Data Institutional
Collection <https://eaw-ckan-dev1.eawag.wroot.emp-eaw.ch>`_. Refer to
internally communicated guidelines or contact the `Eawag Research Data
Management Project \<rdm@eawag.ch\> <rdm@eawag.ch>`_ for help. You can
copy & paste the standard text-snippet below (:ref:`Eawag standard
snippet "preservation" <standard_snippet_repo>`). Note that this does
not necessarily means that all this data will be publicly shared. Data
that will not be shared should be mentioned in :ref:`Section 4.2
<section4.2>`.

1. Check whether there are reasons not to preserve a part of the data
   and mention if there are any. That could apply for example to data that
   
   * is subject to a contractual or legal obligation to destroy data after a certain
     amount of time, or
   * simulation data that can be re-created through computation, or
   * high-volume data that can be downloaded any time from a reliable
     external long-term repository, e.g. climate model output.

2. If there are no exceptions, follow Eawag standard procedure and
   copy & paste the :ref:`Eawag standard snippet "preservation"
   <standard_snippet_repo>`.

3. Check whether you consider any of the data eligible for *Long Term
   Storage*.  Mention those datasets and adapt the standard
   text-snippet below (:ref:`Eawag standard snippet "long-term
   storage" <standard_snippet_lts>`).
  
   This applies to data of long-term institutional or societal
   value. Long Term Storage tries to ensure re-usability of the data at
   a time when the creators of the data, the current custodians, the
   current storage platform, or the currently responsible institution
   (Eawag) are not available anymore. Such data is of high quality
   and consists primarily of unique observations of the environment or
   experimental results. Data flagged as *Long Term Storage* in the
   institutional repository will be reviewed with regard to
   file-formats and documentation.

4. List the file-formats that you are going to upload to the
   institutional repository. (see :ref:`Appendix A: File format
   recommendations <file-formats>`).

.. _standard_snippet_repo:
.. admonition:: Eawag standard snippet "preservation"
   :class: admonition-eawag-standard-snippet
	
   It is Eawag policy to generally preserve *all relevant data* generated
   or used by research projects in the Eawag Research Data Institutional
   Collection. This includes all raw data, all processed data that
   directly underlies the reported results, and all ancillary information
   necessary to understand, evaluate, interpret and re-use the results of
   the study. Data from intermediate steps of the analysis that can be
   re-created from preserved information does not need not to be stored.

.. _standard_snippet_lts:
.. admonition:: Eawag standard snippet "long-term storage"
   :class: admonition-eawag-standard-snippet	
		
   The dataset X and Y will be flagged for *Long Term Storage* upon
   submission to the Eawag institutional collection because they
   represent unique and non-reproducible information about the state of
   the environment and we expect them to be of high quality and of great
   utility for future researchers. Datasets flagged for *Long Term Storage*
   will be subjected to specific measures to preserve data integrity and
   data safety, such as additional backups, regular re-writes to new
   storage media and redundant storage in third-party
   repositories. Additionally, data flagged in this way will be stored
   in file-formats that minimize the chance for format obsolescence.

.. rst-class:: html-toggle
	       
Examples
^^^^^^^^

Example 1
.........

All data from this project will be stored in plain text CSV files
(UTF-8 encoding, no BOM). Text-files containing graphics and layout
will be stored in PDF/A. Microscopy images will be stored as TIFF.
 

4. Data sharing and reuse
=========================

4.1 How and where will the data be shared?
------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    Questions you might want to consider:

    * On which repository do you plan to share your data?
    * How will potential users find out about your data?

    Consider how and on which repository the data will be made
    available. The methods applied to data sharing will depend on
    several factors such as the type, size, complexity and sensitivity
    of data. Please also consider how the reuse of your data will be
    valued and acknowledged by other researchers. (This relates to the
    FAIR Data Principles F1, F3, F4, A1, A1.1, A1.2 & A2)

Instructions
^^^^^^^^^^^^^

1. Check whether there is a well-recognized, specialized data
   repository for the kind of data you are producing. For example, it
   might be standard procedure in your field to submit data to `Gene
   Expression Omnibus <https://www.ncbi.nlm.nih.gov/geo/>`_ or `Array
   Express <https://www.ebi.ac.uk/arrayexpress/>`_. Mention it if you do
   so.

2. Otherwise, you might use the :ref:`Eawag standard snippet "sharing"
   <eawag_snippet_sharing>` below.

.. _eawag_snippet_sharing:
.. admonition:: Eawag standard snippet "sharing"
   :class: admonition-eawag-standard-snippet
	   
   The data from this project will be shared through the public facing
   mirror of the Eawag Research Data Institutional Collection, which
   is expected to go on-line in the first quarter of 2018. This
   repository aims at supporting the FAIR Data Principles to the
   extent possible and provides
   
   * a persistent identifyer (DOI) for each dataset,
   * a rich set of metadata (compliant with the DataCite Metadata Scheme 4.0),
   * file fixity through SHA-2 hashsums for all files,
   * long-term data safety as provided by Eawag/Empa redundant storage
     infrastructure and Eawag’s institutional commitment to keep the
     repository running,
   * a well-documented API (including a subset of the well-known
     SOLR/Lucene query language) for searching, finding and harvesting
     datasets, as well as a web-interface with search- and faceting
     functionality,
   * dissemination of the metadata through the DataCite Metadata Store,
     which is harvested by an increasing number of indexing services,
     such as the Bielefeld Academic Search Engine (BASE), OpenAire, OSF
     SHARE, Google Scholar, …
   * provision of cut & paste text snippets for proper citation, and
   * linking with the associated scholary articles through DORA, the
     repository for publications run by Lib4RI, and through the
     partnership between Crossref and DataCite.

   
.. _section4.2:

4.2 Are there any necessary limitations to protect sensitive data?
------------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_

    Questions you might want to consider:

    * Under which conditions will the data be made available (timing of data release, reason for delay if applicable)?
      
    Data have to be shared as soon as possible, but at the latest at the
    time of publication of the respective scientific output. Restrictions
    may be only due to legal, ethical, copyright, confidentiality or other
    clauses. Consider whether a non-disclosure agreement would give
    sufficient protection for confidential data. (This relates to the FAIR
    Data Principles A1 & R1.1)

Instructions
^^^^^^^^^^^^

1. If you can publish all data at the time of publication just state that.

2. If parts of the data will not be made available at all, state the reason(s).

3. If you intend to publish part of the data *before* the related
   publication is finished, you might state this here.

4. In general, the optimal point in time to publish data that underpins
   a publication is right after the publication has been accepted. In
   case you are not able to publish the data latest at the time of
   publication of the respective output, state the reason(s) for that
   delay. State explicitly *when* exactly you plan to publish it
   though.
   
5. If you are confident that you can make all relevant data public in
   time, you might use the :ref:`Eawag standard snippet "publishing OK
   <eawag_standard_publishing_ok>` below.

.. note::
   
    The SNSF description seems to imply that delayed or forgone
    publication of data is only acceptable for *sensitive* data as
    described in :ref:`Section 2.1 <section2.1>`. We believe there are
    other valid reasons and suggest you wait until this problem
    actually materializes at the end of the project, describe the
    issue in the final DMP, and hope that the SNSF will accept that.

Possible reasons for delayed publication (accepted by SNSF) could
for example include:

* The time necessary to anonymize personal data.
* The need to keep patentable information secret until patent protection applies.

Possible reasons for delayed publication, which are **currently not
accepted** by SNSF, include for example:

* The intent to synchronize the publication of the data with other
  publications (e.g. project report, paper, press release) to
  maximize visibility and impact.
* The intent to base follow-up publications on the data, after the
  project has finished.
* The intent to couple re-use of the data by other groups to an offer for collaboration.
  
.. _eawag_standard_publishing_ok:
.. admonition:: Eawag standard snippet "publishing OK"
   :class: admonition-eawag-standard-snippet
	   
   We expect no limitations with respect to publishing the data. It will
   be made available to the public in full, latest at the time of
   publication of the project report.

.. rst-class:: html-toggle
	       
Examples
^^^^^^^^

Example 1
.........
	    
Our data will include meteorological observations obtained from
MeteoSwiss who prohibit any further distribution of the
data. Therefore we will have to exclude these data from publication.

Example 3
.........

The extensive household survey about water-born diseases poses severe
challenges with regard to anonymization, since simple pseudonymization
might not be sufficient to guard against the identification of
individual households by an inference attack that uses other available
information.

Therefore we will be only able to publish summary statistics together
with the associated article. If a sufficiently anonymized dataset
turns out to still hold scientific value, we will publish it no later
than one year after completion of the project.

Example 4
.........

We expect that the the sampling campaign will yield useful data that
cannot be completely exploited within the frame of this project. We
therefore anticipate a follow-up project based on these data and might
therefore delay the the publication of the full dataset for two years.


	 
4.3 I will choose digital repositories that are conform to the FAIR Data Principles. [``checkbox``]
---------------------------------------------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    The SNSF requires that repositories are conform to the FAIR Data
    Principles (Section 5 of the `guidelines for researchers
    <http://www.snf.ch/en/theSNSF/research-policies/open_research_data/Pages/data-management-plan-dmp-guidelines-for-researchers.aspx>`_,
    SNSF’s explanation of the `FAIR Data Principles
    <http://www.snf.ch/SiteCollectionDocuments/FAIR_principles_translation_SNSF_logo.pdf>`_). If
    there are no repositories complying with these requirements in
    your research field, please deposit a copy of your data on a
    generic platform (see `examples
    <http://www.snf.ch/SiteCollectionDocuments/FAIR_data_repositories_examples.pdf>`_). If
    no data can be shared, this is a statement of principles.

Instructions
^^^^^^^^^^^^

.. raw:: html

    Just check the box: <input type="checkbox" checked="true">


4.4 I will choose digital repositories maintained by a non-profit organisation. [``radio-button yes/no``]
---------------------------------------------------------------------------------------------------------

.. admonition:: SNSF [SNSF2017]_
		
    -> If the answer is no: “Explain why you cannot share your data on a
    non-commercial digital repository.”

    The SNSF supports the use of non-commercial repositories for data
    sharing. Costs related to data upload are only covered for
    non-commercial repositories.
