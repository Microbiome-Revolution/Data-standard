#### media_microbiome_ability.csv

- This file contains the outputs from the experiment to determine the ability of microbiomes to influence wheat shoot weight in varying mediums.
- Data is formatted based on the following metadata:

| **Column**            | **Description**                                                     | **Data Description**                                                                                     |
|-----------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Experiment            | The ID of experiment that has been conducted                        | Categorical, data takes the format "expy", where y is an integer reflecting the order of the experiment in its series | 
| Plant                 | The ID of the plant that has been surveyed within an experiment     | Categorical, data takes the format "plx", where x is an integer reflecting the unique plant in the experiment, beginning at 1|
| Medium                | The medium a plant has been grown in                                | Categorical, either gravel, sand, compost, vermiculite, or perlite                                                    |
| Bacterial_applications | The intensity at which bacteria was applied to the medium and plant | Categorical, either never, limited, or always                                                                         |
| Feed                      | Whether feed was given or not                                                                    | Binary, yes or no format                                                                                                   |
| Dry_weight                       | Weight of above ground biomass after drying.                                                                     |   Numeric, measured in grams.                                                                                                       |
| Germination_rate                       | How many seeds germinated out of the four sown.                                                                    |  Numeric, 1-4                                                                                                        |
