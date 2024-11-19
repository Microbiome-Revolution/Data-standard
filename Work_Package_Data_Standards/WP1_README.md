## The Microbiome Green Revolution's documentation for working with Work-Package 1 (Field Surveys) data and metadata

### There are currently three files associated with Work-Package 1:

#### *dna_quantifications.csv*

- This file contains the outputs from the DNA quantification experiments, following the field sample collection undertaken by Imperial Staff and Farmers.

- Data is formatted based on the following:

| **Column** | **Description**                                                                       | **Data Description**                                                                                                       |
|------------|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Plate      | The plate number used for the DNA quantification.                                     | Data takes the format "px" where x is the plate number. E.g. plate 1 is labelled p1                                        |  
| Well       | The well on a plate that a sample is assigned to on an alphanumeric grid.             | On a 96-well plate, the data is a combination of A-H and 1-12. E.g., First row, fourth column of a plate is A4.            |  
| Temp       | The temperature at which DNA quantification was conducted for a plate.                | Numeric values in Celsius                                                                                                  |
| Wavelength | The excitation and emission wavelengths used to measure fluorescence used on a plate. | Wavelength data in nm, in the format of excitation/x_emission/y. E.g., 485nm excitation, x, 528 emission, y: 485/20_528/20 |
| Quantity   | The quantity of DNA in a well.                                                        | Numeric value in ng.                                                                                                       |                                                        