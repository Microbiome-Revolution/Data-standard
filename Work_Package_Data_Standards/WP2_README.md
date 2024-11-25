## The Microbiome Green Revolution's documentation for working with Work-Package 2 (Lab Experiments) data and metadata

### There are currently three files associated with Work-Package 2. WP2 files are typically separated by the experiment setting, as reflected in the name of the files, due to their different research questions and objectives. 

#### experiment_2.csv

- This file contains the outputs from the DNA quantification experiments, following the field sample collection undertaken by Imperial Staff and Farmers.

- Data is formatted based on the following metadata:

#### yifan_xu_msc_project_2023.csv

- This file contains the outputs of a proof-of-concept experiment to see:
  - How much inoculum we needed to get wheat plants sick
  - Whether the inoculum would persist in soils for up to 2 months without a plant there
  - How soon we would see growth impacts on the plants

- The research was conducted by the student Yifan Xu, who was interested in nitrogen and its interaction with the inoculum. The main take-home that is relevant to the MGR is that different ways of adding the inoculum all resulted in sick plants, making it relevant to WP2 despite its methodological questions and aims.

| **Column** | **Description**                                                                            | **Data Description**                                                                                                                                                                                                      |
|------------|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| Month      | Amount of time elapsed between soil inoculation with Gt, and planting of a wheat seedling. | Treatments were 0 or 2 months                                                                                                                                                                                             |
| Batch      | Indicates when wheat plants were harvested.                                                | Batch 1 = 3 weeks after planting, Batch 2 = 6 weeks after planting, Batch 3 = 9 weeks after planting.                                                                                                                     |
| Pot Number | Individual ID of the microcosm                                                             | Numeric identifier                                                                                                                                                                                                        |
| Nitrogen   | Whether plants were inoculated with nitrogen                                               | N = no (control), Y = 20ml of nitrogen solution (1ml of 7% N plant food in 99ml Dl water)                                                                                                                                 |
| Inoculum   | The amount of inoculum used                                                                | A = 0% Gt (control) <br> B = 0.12% Gt (1g of Gt-infested, crushed oats mixed with 849g soil)<br> C = 1% Gt (8.5g infested oats mixed with 841.5g soil) <br> D = 1% Gt + pure agar plug of the fungus inserted in the pot. |
| Plant size | Plant dry weight                                                                           | Numeric value in g.                                                                                                                                                                                                       |
| Date       | Date of harvest                                                                            | Date value in mm/dd/yyyy                                                                                                                                                                                                  |