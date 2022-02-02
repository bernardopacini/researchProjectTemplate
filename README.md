Research Project Template
=========================

This template provides a starting point for computational research projects.
The aim of this template is to provide a standardized way of working on a project and documenting the work that makes it easily reproducible in the future.
The data in this repository should include all the necessary files, properly configured, to run all of the cases presented in the work, for example to reproduce results in a paper.
The documentation in this repository should provide guidance for every step of the work, from pre-processing, to solving, to post-processing.

To generate the documentation, ensure you have a working Python3 installation with `sphinx` and `sphinx-prompt` installed.
Navigate to the `/doc/` directory and execute:

```
make html
open build/html/index.html
```

To use this template, create a new repository using this template and adjust the fields as necessary.

Repository Structure
--------------------

This part of the README should include a description of the repository structure, showing where each case is stored.
For example, a structure diagram could be:

```
project
│   README.md
│
└───case1
│   │   file1.txt
│   │   file2.txt
│   │
│   └───subfolder1
│       │   file11.txt
│       │   file12.txt
│       │   ...
│
└───case2
│    │   file1.txt
│    │   ...
│
└───doc
│    │   index.rst
│    │   ...
```

Adapt this diagram as needed to show how the repository is set up.

Non-Git Files
-------------

Some files are not git-trackable because they are in binary (non-text) form, because they are very large and would consume too much space, or because their raw data is meaningless and would produce unintelligible git diffs.
Be sure to include these files in the `.gitignore` so that they are automatically not synchronized with the repository.
To handle these files, store them somewhere else, such as Google Drive, and then include a bash stript for downloading the data.
An example script is included in the `inputData/` directory called `getData.sh`

Dependencies
------------

Each research project may have a unique set of dependencies.
Include them here and note if they are necessary or not.
The order is arbitrary, but if there is a convenient way of ordering them it can be helpful for users.
For this template, we need only:

- Python3
- Sphinx

Contributors
------------

List the contributors to the project here, starting with those who did the most work and decreasing through the list.

- Bernardo Pacini
