# The Microbiome Green Revolution's data storage and documentation repository

### The purpose of this repository is to store data that is created using the protocols detailed in the projects [Sample Protocol repository](https://github.com/Microbiome-Revolution/SampleProtocols). This repository should *not* be used for storing data that is irrelevant to the study aims, accessory to main files that are essential to the project and its analyses, or inaccessible data. 

### Before contributing to this repository, please familiarise yourself with the data and metadata principles below for how to structure your files appropriately, including all necessary information outlined in the protocols. 

### This repository is set up using GitHub LFS to store the Microbiome Green Revolution's data and associated metadata, with a primary goal being to keep well documented and compact data, avoiding redundant and duplicated files, using version control.  


# Table of Contents
* [Data Principles](#data-principles)
* [Metadata Principles](#metadata-principles)
* [Directory Structure](#directory-structure)
* [Git Workflow](#git-workflow)

---

### Briefing

Please follow this decision tree to determine whether the data you are trying to include in this repository is appropriate.

 <img src="graphics/decision_tree.svg" width="800" alt="">

---

### Data Principles

**The person responsible for formatting the data and metadata in an appropriately reproducible manner is the one collecting it.** Fundamentally, they are the best to explain the biological meaningfulness of their data and methods, and produce understandable documentation. 

Data consists of the outputs of a field observation or a laboratory instrument formatted into a accessible file rather than direct outputs. This is primarily because of the nature of the project requiring a large amount of data to be spread across an interdisciplinary team, requiring immediate access to usable data. It includes: 
- Quantitative data recorded in a laboratory notebook (e.g. a series of plant heights), transcribed into a spreadsheet 
- Data exported directly from an instrument (e.g. microplate spectrophotometer, real-time PCR machine) into a universal format (e.g. a .csv file) and organised appropriately into a single file
- Raw image files (e.g. in .jpeg or .png format) 
- Raw sequence files (e.g., in fastq format) should **not be included in this repository**

Data file formatting principles for this project should ensure clarity, consistency, and usability across all datasets. The following guidelines should be followed:

- Each file should have a clear and consistent name that reflects its content and purpose. For example, dna quantifications of falmer kit samples should be named ```falmer_kit_dna_quantifications.csv```, to allow additions to be made to the file without naming changes. 
  - Master's student data files should be named as: ```<firstname>_<surname>_<msc/mres>_<year>_<naming structure as above>.csv```
<br> <br>
- Every dataset should include an accompanying metadata markdown file that explains the purpose of the file, named with the same prefix as the file it describes, e.g. the above file's metadata would be named ```falmer_kits_dna_quantifications.md```
<br> <br>
- Columns should have consistent formatting and align with the descriptions provided in the metadata. These descriptions should be detailed, explaining any specific rules or conventions (e.g., plate numbers formatted as ```p1```, ```p2```, etc., and sample IDs that reflect collection details, such as ```7PY.01.18```).
<br> <br>
- All data entries should follow a standard format for each variable. For example, well positions should use an alphanumeric grid system like ```A1``` or ```B12```, and sample IDs should follow a predefined naming convention. that reflects the collection method or source. Numeric fields should adhere to defined ranges or thresholds, while categorical variables (e.g., levels of inoculum or nitrogen treatments) must use consistent, pre-established labels.
   - **The data within columns should not contain values that could be treated as delimiters, such as commas, spaces, tabs, etc.** 
   - **If there are multiple data points within a single cell, it is always best to split the values into a new column to maintain a consistent format that does not require editing to be interpreted and analysed.**  
<br>
- Missing or unused data should be clearly marked using standardised values such as "EMPTY" for values that are intentionally left unused or "NA" for unavailable data. This ensures missing data can be easily identified and managed in subsequent analyses.
<br> <br>
- Files should be structured to facilitate integration into downstream processes, such as statistical analyses or modelling. Each row should correspond to an individual observation (e.g., wells, plants, or samples), and each column should represent a single variable. Every variable has a dedicated column and every observation occupies a single row.



   | Category         | Principle                     | Good Example                             | Bad Example                        |
   |------------------|-------------------------------|------------------------------------------|------------------------------------| 
   | Column Names     | Consistent formatting         | ```sample_id```, ```plant_weight```      | ```SampleID```, ```Plant Weight``` |
   |                  | Descriptive and clear         | ```well_position```, ```dna_quantity```  | ```wp```, ```quantity```           |
   |                  | Standardised convention       | ```snake_case``` (e.g., ```sample_id```) | ```SAMPLEID```, ```sample.id```    |
   |                  | No special characters         | ```plate_number```                       | ```plate#```                       |
   | Data Conventions | Standardised units            | ```μg/μl```, ```g```                     | No units or mixed units            |
   |                  | Uniform date formats          | ```dd/mm/yyyy```                         | mm/dd/yyyy, 2024-Nov-25            |
   |                  | Clear missing data markers    | ```EMPTY```, ```NA```                    | Blank cells, ```0```               |
   |                  | Predefined categorical labels | ```N```, ```Y``` for nitrogen use        | ```Yes```, ```No```, ```N2```      |

<br>

---

### Metadata Principles
The metadata file is integral to our data management plan. It should be possible for an unaffiliated researcher, years in the future, to reconstruct the entire data collection process given the metadata file and its associated raw data file(s). 

A metadata markdown file in this repository should contain a description that has, at a minimum: 
- Enough information to identify the specific experiment from which the data was collected, including date(s) of collection and the identity of the experimenter, and a brief description of the experimental design (e.g. ‘soil microbiome sequence data collected from 100 farms across the UK between April and June 2025;’ ‘MSc project to examine disease severity in wheat inoculated with different strains of G. tritici’)
  - Do not include an experiment description which would be uninterpretable by an unaffiliated researcher (e.g. ‘samples from second passage;’ ‘Amy’s MSc project’)  
- Specific GPS location of the experiment (for field-based experiments/samples)  
- The type of data being collected (e.g. sequence data, index of plant infection level, etc.)   
- Any unique identifiers for the specific output data that will be useful in understanding where it has originated from.

Within the same file, there should be a summary table describing the structure of the raw data set. In this table, the columns of the raw data become rows, with a minimum of a column descriptor, explaining what the data in the column is, and a data descriptor, explaining what format the data within the column is in:

Additionally, there should be an embedded URL to the sample protocol used to create the data files. If a sample protocol is not available, for example because it was produced externally, the metadata file should contain as much information about the collection methods and contents as possible. 

#### Raw Data Table
| Column_1 | Column_2 | Column_3 |
|----------|----------|----------|
| a        | 1        | a1       |

#### Metadata Table
| Columns  | Description                                                            | Data                                                                                                                                   | 
|----------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Column_1 | Column containing alphabetic data                                             | Data contains any of the 26 Latin letters in lower case, between A-Z                                                                               |
| Column_2 | Column containing numeric data                                                | Data contains integers                                                                                                                             |
| Column_3 | Column containing alphanumeric data as a combination of Column 1 and Column 2 | Data is alphanumeric combination of the 26 Latin letters in lower case, and integers, in the form of "xy" where x is the letter and y the integer. |

---

### Directory Structure

Data descriptor files should be placed within the relevant work package directory, with sub-directories containing the data and metadata. If single analyses produce relevant, grouped data sets, then these should be placed into subdirectories in the data repository with their corresponding metadata file in this repository.
 
- **Within each work package directory, please include a ```README.md``` file that outlines the directory structure and a broad purpose of the data.**
- **If you enter a data file into the data repository, and don't include a corresponding descriptor/metadata file here, please know that no one will understand what it is for.** 

An appropriate work package repository would include descriptor files in the following directories in this repository:
```
WP1
|-- README.md
|-- dna_quantification/
|-- |-- dna_quantification_results.csv
|-- |-- dna_quantification_results.md
```

---

# Git Workflow

This section covers all the key steps for working together on a GitHub repository, plus how to handle common issues like merge conflicts and pull errors. Whether you are working on a repository for the first time or contributing for the tenth, this guide is intended as a resource you can revisit whenever needed.

#### Setup and Installation

Before contributing, make sure your tools are ready. Every user needs Git installed, and Sublime Merge provides a visual interface that makes collaboration easier. Even if you have used Git before, checking your setup ensures you avoid small problems later.

To install Git: 

  - **Linux:** `sudo apt install git`
  - **Mac:** `brew install git`

Download and install Sublime Merge from <https://www.sublimemerge.com/>.

Configure your Git identity to link your commits properly:

``` bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

This configuration only needs to be done once on each machine.

------------------------------------------------------------------------

#### Basic Git Concepts

Git tracks changes in a project. A repository (repo) contains your project files. Cloning makes a local copy of a remote repo, allowing you to work on it. Branches let you work safely on features without disturbing the main code. Commits save snapshots of your work, pushing sends them to GitHub, and pull requests propose merging your work back into the main project. Merge conflicts happen when two changes overlap, requiring manual intervention.

 <img src="graphics/git_commands.svg" width="400" alt="">

------------------------------------------------------------------------

#### Typical Git Workflow

The basic cycle remains the same: clone (or pull updates), create a branch, make changes, commit them, push the branch, and create a pull request.

#### 1. Clone the repository

When first joining the project, you will need to clone the repository to get all project files locally. Later on, you will typically just pull new changes instead.

In Sublime Merge: `Repository` \> `Clone Repository` and paste the GitHub URL. This downloads the repo to a local folder.

#### 2. Create a new branch

Before making changes, create a new branch each time. This protects the main code and organizes your work clearly.

In Sublime Merge: `Branch` \> `Create Branch`. Name it meaningfully, e.g., `yourname-update-dictionary`.

#### 3. Make your changes

You can now modify or add files as needed. Git and Sublime Merge will automatically detect and track your changes.

#### 4. Commit your changes

Commits save your work locally. Write small, clear commits to make your history readable and easier to troubleshoot.

In Sublime Merge: stage files, write a short descriptive message, and click `Commit`.

#### 5. Push your branch

After committing, push your branch to GitHub so others can see it.

Click `Push` in Sublime Merge. The first push for a branch may ask you to confirm the branch destination.

#### 6. Create a pull request (PR)

A pull request proposes merging your branch into the main project. Always create a PR after pushing.

Sublime Merge will often suggest this, or you can open GitHub and click "Compare & pull request." Write a clear description of your changes.

#### 7. Review and merge

Other team members will review your PR. You might be asked to revise it, or it may be approved and merged. This process ensures project quality and shared understanding.

------------------------------------------------------------------------

#### Handling Common Problems

#### Problem: Git Pull Error ("Your local changes would be overwritten")

If you have uncommitted changes and attempt to pull updates, Git will block the pull to prevent losing your work.

We want to avoid unintentional overwriting. Resolving this ensures you either safely save or temporarily shelve your local changes.

#### Solution 1: Commit your changes

``` bash
git add README.md
git commit -m "Save local changes before pulling"
git pull
```

This saves your changes first (`add` and `commit`), then integrates remote updates with `pull`.

#### Solution 2: Stash your changes

``` bash
git stash
git pull
git stash pop
```

This temporarily hides your changes with `stash`, pulls the latest remote updates, then reapplies your changes with `stash pop`.

#### Problem: Merge Conflicts

Merge conflicts arise when two sets of changes overlap. Git cannot automatically merge them and asks for your help.

We want to resolve conflicts carefully to preserve all important edits and maintain project integrity.

In Sublime Merge, conflicted files are highlighted. Open them to choose whether to: - Accept "ours" (your version) - Accept "theirs" (incoming version) - Manually edit to merge both versions

After resolving, stage the files and commit to finalize the merge.

------------------------------------------------------------------------

#### Best Practices

Whether it's your first contribution or a routine update, following best practices ensures smooth collaboration: - Always pull the latest main branch before creating a new branch or working. - Create a new branch for each separate task. - Write clear, descriptive commit messages. - Handle conflicts carefully and communicate with teammates if needed. - Delete local and remote branches after merging to keep the project clean.

------------------------------------------------------------------------

#### Quick Reference Cheat Sheet

| Action         | Command                          |
|----------------|----------------------------------|
| Clone repo     | `git clone <repo-url>`           |
| Create branch  | `git checkout -b branch-name`    |
| Stage changes  | `git add .`                      |
| Commit changes | `git commit -m "message"`        |
| Push branch    | `git push -u origin branch-name` |
| Pull latest    | `git pull`                       |
| Stash changes  | `git stash` and `git stash pop`  |
| See branches   | `git branch`                     |
| Delete branch  | `git branch -d branch-name`      |

------------------------------------------------------------------------

