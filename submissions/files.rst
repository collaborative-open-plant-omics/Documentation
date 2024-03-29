.. _files:

=====================
Files Submission
=====================

How to Submit Files
------------------------------

.. hint::

   * See :abbr:`ENA (European Nucleotide Archive)` `assembly submission file types documentation <https://ena-docs.readthedocs.io/en/latest/submit/assembly.html#files-for-genome-assembly-submissions>`__
     for the types of files that can be submitted in COPO for assembly submissions.

   * See :abbr:`ENA (European Nucleotide Archive)` `read submission file types documentation <https://ena-docs.readthedocs.io/en/latest/submit/fileprep/reads.html#accepted-read-data-formats>`__
     for the types of files that can be submitted in COPO for read submissions.

.. seealso::

  * :ref:`How to Delete Files <files-deletion>`
  * :ref:`How to Submit Reads <reads>`
  * :ref:`How to Submit Assemblies <assemblies>`

.. raw:: html

   <hr>

Accessing the Files' Web Page
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Files' web page can be accessed from the **Components** button or **Actions** button associated with a
profile [#f1]_.

.. raw:: html

   <hr>

Use Components' Button to Navigate to Files' Web Page
""""""""""""""""""""""""""""""""""""""""""""""""""""""""

Click the |profile-components-button| button associated with a profile. Then, click the  |files-component-button| from
the popup menu displayed as shown below:

.. figure:: /assets/images/profile/profile_standalone_profile_components_files.png
  :alt: Stand-alone Files' profile component
  :align: center
  :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/profile/profile_standalone_profile_components_files.png
  :class: with-shadow with-border
  :height: 600px

  **Stand-alone Profile Components: Files component button**

.. raw:: html

   <hr>

Use Actions' Button to Navigate to Files' Web Page
"""""""""""""""""""""""""""""""""""""""""""""""""""

Click the |profile-actions-button| button associated with a profile. Then, click the action, **Upload Files** action
from the popup menu displayed as shown below:

.. figure:: /assets/images/profile/profile_standalone_profile_actions_files.png
  :alt: Stand-alone Files' profile action
  :align: center
  :height: 70ex
  :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/profile/profile_standalone_profile_actions_files.png
  :class: with-shadow with-border

  **Stand-alone Profile Actions: 'Upload Files' action**

.. raw:: html

   <hr>


Submit Files from your Local (Computer) System
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Click the |add-files-via-computer-button| button on the Files web page to add a new file by browsing your
   local file system

    .. figure:: /assets/images/files/files_pointer_to_add_files_via_computer_button.png
      :alt: 'Add new file by browsing local file system' button
      :align: center
      :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_pointer_to_add_files_via_computer_button.png
      :class: with-shadow with-border

      **Files web page: 'Add new file by browsing local file system' button**

   .. raw:: html

      <br>

#. An **Upload File** dialogue is displayed. Click the **Upload** button to choose a file from your local system.

    .. figure:: /assets/images/files/files_upload_file_dialogue.png
      :alt: Upload File dialogue
      :align: center
      :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_upload_file_dialogue.png
      :class: with-shadow with-border

      **Files submission: Upload File dialogue**

   .. raw:: html

      <br>

#. The new file(s) will be displayed on the **Files** web page after a successful submission.

    .. figure:: /assets/images/files/files_uploaded1.png
      :alt: File(s) submitted
      :align: center
      :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_uploaded1.png
      :class: with-shadow with-border

      **Files submission: Files' web page displaying the uploaded file(s)**

    .. raw:: html

       <br><br>

    .. hint::

      To add more files from your local system, click the |add-files-via-computer-button1| button (once files have been
      submitted to the profile) as an alternative to clicking the |add-files-via-computer-button| button.

.. raw:: html

   <hr>

Submit Files via the Terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _files-submission-via-terminal-hint:

.. hint::

      If you encounter the server certificate error, ``curl: (60) Peer's Certificate issuer is not recognized.``, please
      perform one of the the following resolutions:

      * **Resolution #1**: Run the command below in the terminal (if you have ``sudo`` rights on your device)

         .. code-block:: bash

            $ sudo apt-get install ca-certificates

        .. centered:: **OR**

      * **Resolution #2**: Replace ``https`` with ``http`` in the generated command
        indicated :ref:`here <files-submission-via-terminal-copy-commands>` then, run the command in the terminal again.

#. Click the |add-files-via-terminal-button| button on the Files web page to add a new file from a cluster via the
   terminal.

    .. figure:: /assets/images/files/files_pointer_to_add_files_via_terminal_button.png
      :alt: 'Add new file via terminal' button
      :align: center
      :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_pointer_to_add_files_via_terminal_button.png
      :class: with-shadow with-border

      **Files web page: 'Add new file via terminal' button**

   .. raw:: html

      <br>

#. A **Move Data** dialogue is displayed. Follow the instructions displayed then, click the **Process** button to submit
   the file(s) to the profile.

    .. figure:: /assets/images/files/files_move_data_dialogue.png
      :alt: Move Data dialogue
      :align: center
      :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_move_data_dialogue.png
      :class: with-shadow with-border
      :height: 400px

      **Files submission: Move Data dialogue**

   * .. figure:: /assets/images/files/files_move_data_dialogue_terminal_input1.png
        :alt: Terminal with command inputted
        :align: center
        :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_move_data_dialogue_terminal_input1.png
        :class: with-shadow with-border

        **Input** $ ``ls - F1`` **command in the terminal**

        .. raw:: html

           <br>

   * .. figure:: /assets/images/files/files_move_data_dialogue_with_details1.png
        :alt: Move Data dialogue with details inputted
        :align: center
        :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_move_data_dialogue_with_details1.png
        :class: with-shadow with-border
        :height: 400px

        **Move Data dialogue: Input the filename(s) returned after having ran the** $ ``ls - F1`` **command in the
        terminal. Then, click the** ``Process`` **button.**

        .. raw:: html

           <br>

   .. _files-submission-via-terminal-copy-commands:

   * .. figure:: /assets/images/files/files_move_data_dialogue_with_details2.png
        :alt: Move Data dialogue with result (a command) after having clicked the "Process" button
        :align: center
        :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_move_data_dialogue_with_details2.png
        :class: with-shadow with-border
        :height: 400px

        **Move Data dialogue: Command outputted after having clicked command in the** ``Process`` **button. Copy the
        command displayed.**

        If you encounter the server certificate error, ``curl: (60) Peer's Certificate issuer is not recognized.``,
        please see the :ref:`hint <files-submission-via-terminal-hint>` at the beginning of this section.

   * .. figure:: /assets/images/files/files_move_data_dialogue_terminal_input2.png
        :alt: Terminal with command pasted
        :align: center
        :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_move_data_dialogue_terminal_input2.png
        :class: with-shadow with-border

        **Paste the copied command in the terminal**

        .. raw:: html

           <br>

   .. raw:: html

      <br>

#. The new file(s) will be displayed on the **Files** web page after a successful file submission via the terminal i.e.
   after the command has been executed successfully in the terminal.

    .. figure:: /assets/images/files/files_uploaded2.png
       :alt: Files submitted
       :align: center
       :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_uploaded2.png
       :class: with-shadow with-border

       **Files submission: Files' web page displaying the uploaded file(s)**

    .. raw:: html

       <br><br>

    .. hint::

       To add more files via the terminal, click the |add-files-via-terminal-button1| button (once files have been
       submitted to the profile) as an alternative to clicking the |add-files-via-terminal-button| button.

.. raw:: html

   <hr>

.. _files-deletion:

How to Delete Files
--------------------

Click the desired file from the list of files displayed on the Files' web page. Then, click the **Delete** button
(located in the top-right corner of the table) as shown below:

.. figure:: /assets/images/files/files_pointer_to_delete_file_button.png
  :alt: Delete files button
  :align: center
  :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_pointer_to_delete_file_button.png
  :class: with-shadow with-border

  **File deletion: Click the "Delete" button to remove the highlighted file from the profile**

.. figure:: /assets/images/files/files_deleted.png
  :alt: Files deleted successfully
  :align: center
  :target: https://raw.githubusercontent.com/collaborative-open-plant-omics/Documentation/main/assets/images/files/files_deleted.png
  :class: with-shadow with-border

  **File deletion: File has been deleted**

.. raw:: html

   <br>

.. raw:: html

   <hr>

.. rubric:: Footnotes

.. [#f1] Also known as COPO profile. See: :term:`COPO profile  or work profile<COPO profile>`.

.. raw:: html

   <br><br>

..
    Images declaration
..
.. |files-component-button| image:: /assets/images/buttons/components_files_button.png
   :height: 4ex
   :class: no-scaled-link

.. |add-files-via-computer-button| image:: /assets/images/buttons/add_files_via_computer_button.png
   :height: 4ex
   :class: no-scaled-link

.. |add-files-via-terminal-button| image:: /assets/images/buttons/add_files_via_terminal_button.png
   :height: 4ex
   :class: no-scaled-link

.. |add-files-via-computer-button1| image:: /assets/images/buttons/add_files_via_computer_button1.png
   :height: 4ex
   :class: no-scaled-link

.. |add-files-via-terminal-button1| image:: /assets/images/buttons/add_files_via_terminal_button1.png
   :height: 4ex
   :class: no-scaled-link

.. |profile-actions-button| image:: /assets/images/buttons/profile_actions_button.png
   :height: 4ex
   :class: no-scaled-link

.. |profile-components-button| image:: /assets/images/buttons/profile_components_button.png
   :height: 4ex
   :class: no-scaled-link
