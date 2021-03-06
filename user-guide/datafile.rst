==============
Introduction
==============

Datafile is one of the main components of a COPO profile. Within the datafile page, the user will be able to upload, inspect (view uploaded files), and describe datafiles (attribute metadata).

.. image:: /images/datafile-page.jpg

The screenshot shows the datafile page, with tabs to represent the key tasks mentioned (i.e., upload, inspect, and describe). Clicking a tab reveals the underlying view and controls to carry out actual work.


.. _datafile-upload-label:

========
Upload
========

Follow these steps to upload datafiles to COPO:

1. Click the **Upload** tab to reveal the file upload view (see screenshot above).
2. Within the upload pane, click the **Select files...** button. This should open a file browser.
#. Select one or more files to upload.

The selected files are uploaded to COPO. The upload process might involve compressing the datafiles (for large files), and `hashing` (for subsequent integrity verifications).

The process is demonstrated using the screenshots below. Two files were selected for upload; each approximately :code:`2GB` in size. The files are uploaded, compressed, and hashed. 

.. image:: /images/datafile-zipped.jpg


.. image:: /images/datafile-hashing.jpg

.. warning::
   In order to speed up the upload process, and for general user experience, it is advised that large files (e.g., size >=1GB) be compressed (using gzip) before  uploading them to COPO.



In the screenshot below, the displayed files have successfully been through the upload process. For each file, the name, extension (:code:`.gz` added if compressed), size (which now reflects the modified size after compression), and the hash value are displayed.

.. image:: /images/datafile-upload-finish.jpg

.. note::
   While COPO is positioned to broker the submission of data to remote repositories, it is not equipped to serve as a `silo` for datafiles. Uploaded datafiles are held only for a short period of time, pending deposition of such to remote repositories.


========
Inspect
========
The inspect pane provides a view to the datafiles within a profile.

.. image:: /images/datafile-inspect.jpg

The presented view (see screenshot above) displays the two files uploaded to COPO. The file type has been identified as `fastq`. In general, the inspect view is consistent [#consistency_in_view]_ with the view discussed under the :ref:`sample detail view <sample-detail-view>` section. The user can reference that section for a description of overlapping controls. 

.. note::
   COPO tries to determine, and display accordingly, the type of an uploaded datafile. Where this is not possible, the type will be displayed as `unknown`. However, this does not disrupt the actions the user can perform on such files.
   

Tasks can be performed on a single datafile or a group of datafiles (bundle). Some of the relevant tasks defined for datafiles are:

Describe
	Click this button to describe selected datafiles. This would activate the description wizard, enabling the process of metadata attribution for the target files. 
	
	As mentioned, the user can either describe a single file or a bundle of files. This process will be discussed subsequently in more detail.  
	
Discard Metadata
	 Click this button to remove associated metadata on selected datafiles. 
	 
	 .. hint::
	    A **metadata indicator** is a visual cue beside a datafile record with information about its metadata level. In the screenshot above, the metadata indicator is represented by the red square beside a datafile record, and this indicates the absence of metadata. The user can hover over the indicator for state information. 


=======================
Describe
=======================
COPO supports, and provides relevant templates for, the description and submission of datafiles to a number of repositories (e.g., `ENA <https://www.ebi.ac.uk/ena/>`_, `Figshare <https://figshare.com>`_). 

Before embarking on datafile description, the user might want to give some thought about the end-point (i.e., the intended repository) of the target datafiles. For instance, certain file types might only be suitable for submission to specific repositories.

Irrespective of the description template used or the intended repository, the general process of datafile description is relatively similar. Any discrepancy in using any particular template will be highlighted where relevant.


.. _select-desc-target-label:

Select the target files
--------------------------
The first step involves selecting the files to be described or the **description bundle**. The user can select a single file or multiple files. 

.. note::
	Multiple file description is useful (and possible) in situations where the files to be described would have similar metadata, and be potentially submitted to the same repository.
	
1.	Select the files to be described
2.	Click the **Describe** button

.. image:: /images/datafile-select-files.jpg

The datafiles are validated for suitability of being described together (bundled), and the user would be expected to confirm the `bundling` action (see the screenshot below).

.. note::
	The confirmation dialog `might` not be displayed in a single file description.

.. image:: /images/datafile-bundling-confirm.jpg

3. Click **Continue** to confirm the bundling

The view should switch to display the description wizard.


.. _datafile-wizard-label:

Datafile description wizard
---------------------------------

.. image:: /images/datafile-description-wizard.jpg
.. image:: /images/datafile-description-wizard-2.jpg

The screenshots above provide an illustration of the datafile description wizard. The wizard, as observed in the screenshot, is laid out into different logical work sections, which include:

1. Action buttons
2. Stage navigation buttons
#. Stage label
#. Description metadata or stage form
#. Description bundle
#. Info/Help panes


Action buttons
----------------

These are the group of buttons located to the top left hand corner (:ref:`top left hand side, highlighted in red <datafile-wizard-label>`).

Discard Description
   Clicking this action button will discard the description and associated metadata to the description bundles. The view will switch back to the **Inspect** pane.
   
   .. warning::
   	The discard description action deletes every description metadata associated with datafiles in the description bundle. Given the implication of this action, the user will be required to confirm the action before proceeding.
	
Exit Description
   Clicking this button terminates the description (and the wizard). The view will switch back to the **Inspect** pane.
   
   .. note::
    The exit description action, unlike the discard description action, preserves the metadata attributed to the description bundle. Description metadata, up to but not including the current stage, is saved and the user can continue from this `breakpoint` at a later stage.

Stage Info
   Clicking this displays relevant information to the current stage (e.g., metadata input required in the stage). Same information can be found on the **Info** panel (:ref:`right side hand side <datafile-wizard-label>`).
   

.. _datafile-wizard-nav-label:

Stage navigation buttons
--------------------------

The stage navigation buttons (:ref:`right hand side, highlighted in green <datafile-wizard-label>`) are the **Prev** and **Next** buttons that enable the user to go back and forth through the stages of the wizard. 

By clicking **Next**, the user-supplied input in a current stage is saved, and the wizard transitions to a new stage. The user can also go back through the stages, to update or view previous entries, by clicking the **Prev** button.

Stage label
---------------

The stage label is located on the same level (:ref:`left hand side, below the action buttons <datafile-wizard-label>`) as the stage navigation buttons. 

The current stage appears in a bold colour (blue in this case). Non-active stages are usually greyed out. In addition to the label, each stage has a stage id (or serial number). This is displayed alongside the label, and provides a convenient way of referencing a stage.

In the :ref:`screenshot <datafile-wizard-label>` above, the current stage, which happens to be the first stage of the wizard, is labelled `Target Repo`, with a serial number of `1`.


.. hint::
 Stage labels can be used for navigation purposes. For instance, while in, say, `stage 3` of the wizard, the user can click the label of a previous stage, say, `stage 1` to quickly jump back to that stage.

New stages are presented to the user based on inputs in previous stages. Therefore, choices previously made by the user can potentially lead to a different path, or entirely different sequence of stages, through the wizard.

.. note::
 While it may be possible to quickly jump back to a previous stage by clicking the stage label, similar action is constrained in the opposite direction. The user will have to click the **Next** button to proceed again through the visited stages. This enables the wizard to revalidate the sequence of stages to be presented to the user.
 
 
Description metadata
---------------------------
The description metadata section holds the actual form for obtaining user input (:ref:`middle section of screenshot <datafile-wizard-label>`). Each stage presents a different form for obtaining metadata relevant to the stage. In the  referenced screenshot, for instance, the user is required to select the target repository for the datafiles.

Click the  **Next** button, after filling out the form in a stage, to proceed to the next stage (see: :ref:`datafile-wizard-nav-label`).

Description bundle
---------------------------
The description bundle section is located below the description metadata section, and to the bottom of the description wizard (see: :ref:`datafile-wizard-label`). This section lists currently described datafiles in a tabular format. The following features are provided, which will be demonstrated in relevant contexts:

* **Add/remove from bundle:** Datafiles can be added to, or removed from, the description bundle at any stage of the description.

* **Individual file update:** The user can access and, in many cases, edit metadata for individual datafiles in the description bundle.

* **Metadata viewing:** The view button (green plus sign to the left of a datafile, see: :ref:`datafile-wizard-label`) beside a datafile provide a means of viewing metadata assigned to the datafile in the stage. This is particularly useful in situations that datafiles in the bundle may potentially have different metadata.

* **Bundle subsetting:** The description bundle section has a search functionality for filtering datafiles in the bundle. This functionality may be used in conjunction with record selection controls such as **Select all**, **Select filtered**, and **Select none** to apply metadata (or perform other tasks) to subsets of datafiles in the description bundle. This is a way of `subsetting` the description bundle. 

As mentioned, these features will be demonstrated subsequently in relevant contexts.

Info/Help panes
-------------------------
The info and help panels are located to the right side of the wizard (see: :ref:`datafile-wizard-label`). The info pane displays information about the current stage of the wizard. The help pane provides context-based help about the datafiles component in general. It also includes topics specific to datafiles description. It has a search feature that can be explored to filter on keywords.


So far, a general overview of the datafile page has been provided, highlighting key aspects of the UI. The sections that follow will draw on this, to provide a more detailed illustration of datafile description. 

As mentioned, COPO provides a number of templates to support the description of datafiles. These templates are tailored, by defining a minimum set of metadata requirements, to support submission of the datafiles to different target repositories supported in COPO. The first of this to be considered is the submission of raw sequence reads to the `European Nucleotide Archive (ENA) <https://www.ebi.ac.uk/ena>`_.


===============================
Sequence Reads Description
===============================
COPO provides a template for describing raw sequence reads files, which will subsequently enable the submission of the files to the ENA. In this section, a detailed description of describing datafiles intended for the ENA (sequence reads) is provided.

The user would usually begin by, first, uploading the datafiles to COPO, then selecting them for description (see: :ref:`selecting target files <select-desc-target-label>`). The screenshot below highlights the first stage of the description process, after initialising the wizard.

.. _ena-target-repo-label:

Target Repo
---------------

.. image:: /images/datafile-target-repo-ena.jpg

The first stage of the wizard is the **Target Repo**. In this stage, the user gets to select the target repository where the described files will be deposited. The default target repository is `ENA - Sequence Reads`.


.. note::
 The choice of a target repository specifies the description template or the metadata requirement to be engaged for the description.  

.. warning::
 Changing the **Target Repo** can impact the current description in different ways, and the user will usually be prompted for a confirmation before proceeding with the action. 
 
Selecting a different **Target Repo** will result in a different description template being activated. The change in  template actually comes into effect when the user transitions to a different stage of the wizard. The following impact can be observed: 

* loss of any previous metadata attributed to the datafile bundle  
* change in the sequence of steps presented to the user

.. _singular-stage-label:

The target repo stage is a `singular stage`.

.. hint::
 A singular stage is one in which all the datafiles in the description bundle share the same metadata. That is, any metadata supplied in the stage will apply to all bundle items.
 
The following points are applicable to a singular stage: 

* Any metadata supplied in the stage will be applied to all the datafiles in the description bundle. 
* The record selection buttons (i.e., **Select all**, **Select filtered**, and **Select none**) are disabled, implying  that the user can't carry out `subsetting` of the description bundle.
* In line with the previous points, all the records in the bundle are selected or highlighted.  
* A  message (top of the **Description Metadata** section of the wizard) is displayed to inform the user about the intended UI adjustments and the impact on the metadata attribution.

Click the **Next** button, when done in a stage, to proceed to the next stage. 

.. warning::
 Clicking the **Next** button results in the wizard actually saving the entries made in a stage. Exiting the wizard before saving any changes might result in loss of entries made in that stage.
 

.. _ena-study-type-label:

Study Type
---------------

.. image:: /images/datafile-study-type.jpg

Select the **Study Type** from the list. The option made here further constrains the wizard to a specific metadata specification. Notice here that the **Study Type** stage is also a `singular stage`; implying that only one study type is (currently) permissible in any description session.

Select an option, and click the **Next** button to proceed to the next stage. 


.. _ena-sample-label:

Sample
---------------

.. image:: /images/datafile-sample-1.jpg

In the **Sample** stage, biological samples can be linked to datafiles in the description bundle. Listed samples (see screenshot above) are those that meet the following criteria:

* Have been defined in COPO prior to initiating the description wizard (see: :doc:`Samples <sample>` for more information on how to create samples)
* Based on the **COPO Standard** sample type
* Belong to the same profile

.. _non-singular-stage-label:

The user can select a single sample to link to all the datafiles in the description bundle (1 sample to many datafiles). Alternatively, one sample can be linked to one datafile or a subsets of datafiles in the bundle. These options are explored further:

.. note::

   So far, the sample stage is the first *non-singular* stage to be discussed. All the options described below are also applicable to every stage of the wizard that isn't a :term:`singular stage<Singular stage>`.    

1. **Single sample to all datafiles:** A single sample can be linked to all the datafiles in the description bundle as follows:
  
  * With reference to the screenshot above, set the button to **Yes** in response to the question highlighted in red (this is the default option) 
  * Under the **Description Metadata** section, select a sample from the dropdown list
  * Click the **Next** button to (apply the changes, and) proceed to the next stage
  * Note: this option makes the stage to behave like a *singular* stage

.. image:: /images/datafile-sample-2.jpg
 
2. **Single sample to subset of datafiles:** A single sample can be linked to a subset of datafiles in the description bundle as follows:
  
  * With reference to the screenshot above, set the button to **No** in response to the question highlighted in red
  * Under the **Description Metadata** section, select a sample from the dropdown list
  * Select the target subset of datafiles under the **Description Bundle** section
  * Click the apply button (highlighted in green in the screenshot above)
  * Repeat the above steps for as many subsets in the description bundle as required
  * Click the **Next** when done to proceed to the next stage

.. image:: /images/datafile-sample-3.jpg 

3. **Single sample to single datafile:** A single sample can be linked to a single datafile as follows:
  
  * Follow the steps described in option 2 above, or:
  * Set the button to **No** in response to the question highlighted in red (see screenshot under option 2)
  * Click the plus (+) icon beside each datafile, under the **Description Bundle** section, to reveal a metadata form specific to that datafile (see screenshot above)
  * Click the apply button to save supplied entry, and to proceed to the next datafile (see the screenshot above)
  * Click the **Next** button, when done with all the entries, to proceed to the next stage
 

.. _ena-libcon-label:

Library Construction
---------------------

.. image:: /images/datafile-lib-construction.jpg

As part of the metadata attribution in the **Library Construction** stage, the **Library layout** (PAIRED or SINGLE) needs to specified (default option is **SINGLE**). For paired reads (by selecting the **PAIRED** option), the user, at a later stage, will have to specify how the datafiles may be paired. More on this later.


.. _ena-sequencing-label:

Nucleic Acid Sequencing
-------------------------

.. image:: /images/datafile-sequencing.jpg

In the **Nucleic Acid Sequencing** stage, information about the sequencing technique used is requested. Select the relevant option from the dropdown list. Click the **Next** when done to proceed to the next stage.


.. _ena-pairing-label:

Datafiles Pairing
-------------------------

.. image:: /images/datafile-pairing-1.jpg

The **Datafiles Pairing** stage provides a platform for the user to specify how datafiles in paired reads can be paired. COPO provides a suggestion of pairings for the datafiles based on the file names. This process is captured in the screenshot above.

* Select all or any of the rows and click **Apply** to accept the suggestion (notice the **Select all** in the screenshot above). 
* Click **Cancel** to reject the suggestion and manually pair files.


To manually pair files, select any two files in the Description Bundle, click **Pair** in the confirmation box presented to confirm the pairing. This procedure is captured in the screenshot below. 

.. image:: /images/datafile-pairing-3.jpg

All paired datafiles are displayed under **Paired Datafiles** section (right-hand side table on the screenshot below). Within this section, previously paired files can be unpaired by clicking the red icon beside a pair. 

.. image:: /images/datafile-pairing-2.jpg

===============================
Figshare Description
===============================





.. rubric:: Footnotes

.. [#consistency_in_view] Some level of UI consistency is maintained, were possible, across all profile components.
