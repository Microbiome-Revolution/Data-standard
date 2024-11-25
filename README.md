# The Microbiome Green Revolution's documentation for working with data and metadata

This documentation standardises the formatting of sequence data files and sample metadata to comply with reproducible and communicable industry standards. The FAIR principles—Findability, Accessibility, Interoperability, and Reusability—apply directly to data naming conventions of the Microbiome Green Revolution project, ensuring our datasets are well-organised, understandable, and universally usable. Below is an outline of how FAIR principles guide effective data naming practices:
1. Findable
   - **Descriptive Names:** Data files and variables should have meaningful, descriptive names that clearly indicate their content or purpose. For example, names should include project identifiers, experiment types, or dates where relevant.
   - **Consistent Formatting:** Use consistent naming conventions across all files and datasets to make them easier to locate in large repositories. For instance, always use the same date format (e.g., YYYY-MM-DD) or structure (e.g., Project_Condition_Date).
   - **Unique Identifiers:** Ensure each dataset or file name is unique within the context of the project or repository, avoiding duplication or ambiguity.

2. Accessible
    - **Human-Readable Names:** Names should be easy to interpret by both humans and machines, avoiding overly cryptic codes or excessive abbreviations.
    - **No Special Characters:** Avoid spaces, special characters, or symbols in names that might interfere with software or database queries. Instead, use underscores (_) or hyphens (-) to separate words.
    - **Logical Organisation:** Files should be systematically named and stored to allow straightforward navigation, supporting accessibility within and across systems.

3. Interoperable
    - **Standardised Conventions:** Adopt widely accepted naming conventions that are compatible with various software, systems, and disciplines. For instance, follow established formats like snake_case or camelCase.
    - **Versioning:** Include version numbers or timestamps in file names to clarify relationships between iterations (e.g., Dataset_v1 or Data_2024-11-25).
    - **Avoid Context Dependency:** Names should stand alone without requiring external context to interpret their meaning, ensuring compatibility across systems and teams.

4. Reusable
    - **Clear Metadata Alignment:** Ensure naming conventions align with metadata descriptions, enabling future users to understand the data’s structure and content without additional clarification.
    - **Temporal and Contextual Consistency:** Data names should be timeless, avoiding transient references (e.g., "latest" or "temp") that lose meaning over time.
    - **Scalable Conventions:** Use naming patterns that can scale as the dataset grows, accommodating new files or variables without disrupting the established system.

[//]: # (For raw DNA sequence reads &#40;.fastq&#41;, see "SRA")

[//]: # (For metagenome-assembled-genomes &#40;MAG&#41;, bacteriophages, and other assembled genome sequences &#40;.fasta&#41;, see "Genbank")

[//]: # (For sample metadata formatting examples and conventions, see "Metadata")

#### Data file formatting principles for a multidisciplinary biology project should ensure clarity, consistency, and usability across all datasets. The following guidelines should be followed:

1. **File Naming and Metadata:** Each file should have a clear and consistent name that reflects its content and purpose, such as including experiment identifiers or batch numbers (e.g., ```dna_quantifications.csv``` or ```sequencing_qc.csv```). Every dataset should include accompanying metadata that explains the purpose of the file, the meaning of each column, and the format and units of the data. For instance, numerical values such as DNA quantities should clearly specify units (e.g., ```μg/μl```), and dates should follow a consistent format, such as ```dd/mm/yyyy```.

2. **Column Names and Data Description:** Column names should be consistent across all files, using a clear convention like ```snake_case``` or ```camelCase```. For example, columns like plate, well, and sample should have consistent formatting and align with the descriptions provided in the metadata. These descriptions should be detailed, explaining any specific rules or conventions (e.g., plate numbers formatted as ```p1```, ```p2```, etc., and sample IDs that reflect collection details, such as ```7PY.01.18```).

3. **Data Consistency and Standardisation:** All data entries should follow a standard format for each variable. For example, well positions should use an alphanumeric grid system like ```A1``` or ```B12```, and sample IDs should follow a predefined naming convention that reflects the collection method or source. Numeric fields should adhere to defined ranges or thresholds, while categorical variables (e.g., levels of inoculum or nitrogen treatments) must use consistent, pre-established labels.

4. **Handling Missing Data:** Missing or unused data should be clearly marked using standardised values such as "EMPTY" for wells that are intentionally left unused or "NA" for unavailable data. This ensures missing data can be easily identified and managed in subsequent analyses.

5. **Data Structure for Analysis:** Files should be structured to facilitate integration into downstream processes, such as statistical analyses or modelling. Each row should correspond to an individual observation (e.g., wells, plants, or samples), and each column should represent a single variable. A tidy data structure should be maintained, where every variable has a dedicated column and every observation occupies a single row.


| Category         | Principle                      | Good Example                                | Bad Example                        |
|------------------|--------------------------------|---------------------------------------------|------------------------------------| 
| Column Names     | Consistent formatting          | ```sample_id```, ```plant_weight```         | ```SampleID```, ```Plant Weight``` |
|                  | Descriptive and clear          | ```well_position```, ```dna_quantity```     | ```wp```, ```quantity```           |
|                  | Standardised convention        | ```lowerCamelCase``` (e.g., ```sampleId```) | ```SAMPLEID```, ```sample.id```    |
|                  | No special characters          | ```plate_number```                          | ```plate#```                       |
| Data Conventions | Standardised units             | ```μg/μl```, ```g```                        | No units or mixed units            |
|                  | Uniform date formats           | ```dd/mm/yyyy```                            | mm/dd/yyyy, 2024-Nov-25            |
|                  | Clear missing data markers     | ```EMPTY```, ```NA```                       | Blank cells, ```0```               |
|                  | Predefined categorical labels  | ```N```, ```Y``` for nitrogen use           | ```Yes```, ```No```, ```N2```      |


#### Working within this repository

Data descriptor files should be placed within the relevant work package directory. For each data file in the **<link to data repository once it's set up>** there must be a metadata or data descriptor file in this repository. If the structure of the data sets within the WP directories should reflect the data directories, meaning if single analyses produce relevant, grouped data sets, then these should be placed into subdirectories in the data repository with their corresponding metadata file in this repository.   

