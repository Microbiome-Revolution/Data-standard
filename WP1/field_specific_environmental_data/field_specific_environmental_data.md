#### *field_specific_environmental_data.csv*

- This file contains the descriptors for the columns (questions) in the field history survey received from Farmers.

- Data is formatted based on the following metadata:

| **Column** | **Description**                                                                       | **Data Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| site_name    | Refers to field sampled. Name is based on the postcode of the site (or farm). Therefore, postcode SL5 7PY, 7PY is the last 3 characters of the farm postcode; 01. is the field number (In the event that there are multiple fields to be sampled. If there is only one field, label should remain 01.) And XX is sample e.g. 18. So 7PY.01.18 is the 18th sample in the first field from the farm with postcode SL5 7PY.     | Latin letters and Hindu-Arabic system digits E.g 7PY.01.18                     |  
| gps_latitude       | Geographical positioning system showing latitudinal points as obtained from Google maps.             | Hindu-Arabic system digits e.g. 51.409056,                                                                                                                                                                                                                                                                                                                          |
| gps_longitude     | Geographical positioning system showing longitudinal points as obtained from Google maps.                  | Hindu-Arabic system digits e.g. -0.640111 | 
| collection_day | Day samples were collected | 01, 02, 03,  …, 31                                                                                                                                                                                                                                                                                                                                                          |
| collection_month   | Month samples were collected                                                 | 01, 02, …, 12                                                                                                                                                                                                                                                                                                                                                                                                                                                 |    
| collection_year | Year samples were collected | 2024, 2025 |
| crop_rotation_primary_y0 | The wheat variety planted year of sampling | Winter wheat - KWS Vibe, SY Cheer, Skyfall, KWS Zyatt, Crusoe, (New) RGT Goldfinch (BYDV), KWS Extase, KWS Palladium, KWS Ultimatum, Bamford, LG Astronomer, Blackstone, Skyscraper, RGT Bairstow, LG Tapestry, LG Beowulf, Oxford, KWS Dawsum, Fitzroy, KWS Cranium, SY Insitor, RGT Grouse (BYDV), Spring wheat -(KWS Ladum, Nissaba, Mulika, Cochise, Hexham) |
| crop_rotation_companion y0 | Companion crop planted the year of sampling | Grassland, Barley, Forage maize, Oats, Legumes (Beans, Peas, Vetch, Fallow), Oilseed rape, Sugar beet, Potatoes, Other |
| crop_rotation_primary_y1 | Crop planted 1 year prior to sampling | Maize forage, Oats, Barley, Grass ley, Winter wheat, Spring wheat, Other |
| crop_rotation_companion_y1 | Companion crop planted 1 year prior to sampling | Grassland, Barley, Forage maize, Oats, Legumes (Beans, Peas, Vetch, Fallow), Oilseed rape, Sugar beet, Potatoes, Other |
| crop_rotation_primary_y2 | Crop planted 2 years prior to sampling | Maize forage, Oats, Barley, Grass ley, Winter wheat, Spring wheat, Other |
| crop-rotation_companion_y2 | Companion crop planted 2 years prior to sampling | Grassland, Barley, Forage maize, Oats, Legumes (Beans, Peas, Vetch, Fallow), Oilseed rape, Sugar beet, Potatoes, Other |
| crop_rotation_primary_y3 | Crop planted 3 years prior to sampling | Maize forage, Oats, Barley, Grass ley, Winter wheat, Spring wheat, Other |
| crop_rotation_companion_y3 | Companion crop planted 3 years prior to sampling | Grassland, Barley, Forage maize, Oats, Legumes (Beans, Peas, Vetch, Fallow), Oilseed rape, Sugar beet, Potatoes, Other |
| crop_rotation_primary_y4 | Crop planted 4 years prior to sampling | Maize forage, Oats, Barley, Grass ley, Winter wheat, Spring wheat, other |
| crop_rotation_companion_y4 | Companion crop planted 4 years prior to sampling | Grassland, Barley, Forage maize, Oats, Legumes (Beans, Peas, Vetch, Fallow), Oilseed rape, Sugar beet, Potatoes, Other |
| take_all_seen | Response to whether Take-All has been observed or not | Yes, No | 
| take_all_evidence | Observed indications of the Take-All diseases in their wheat fields over the years | None, Black lesions on roots, Reduced yields, Premature death, Bleaching/discolouration, Lower tillering, Other (please specify) |
| take_all_time | Time frame in which the Take-All disease has been observed in the field. | One yea, Two years, Three years, Four years, Five or more years |
| fertiliser_use_nitrogen | Response to wheather or not Nitrogen based fertilizer has been applied to the fields | Yes, No |
| fertiliser_use_phosphous | Response to wheather or not Phosphorus based fertilizer has been applied to the fields | Yes, No |
| fertiliser_use_potassium | Response to wheather or not Potassium based fertilizer has been applied to the fields | Yes, No |
| fertiliser_use_micronutrients | Response to wheather or not Micronutrient fertilizer has been applied to the fields | Yes, No |
| fertiliser_use_other | Response to wheather or not Other types of fertilizers has been applied to the fields | Yes, No |
| fertiliser_application_rate_monthly | Response to temporal rate at which fertilisers have been applied to the field Monthly |  Yes, No |
| fertiliser_application_rate_every_six_months | Response to temporal rate at which fertilisers have been applied to the field Every six months |  Yes, No |
| fertiliser_application_rate_yearly | Response to temporal rate at which fertilisers have been applied to the field Yearly |  Yes, No |
| fertiliser_application_rate_every_two_years | Response to temporal rate at which fertilisers have been applied to the field Every two years |  Yes, No |
| fertiliser_application_rate_every_other | Response to temporal rate at which fertilisers have been applied to the field at other rates |  Yes, No |
| At what rate has this fertiliser combination been applied? | Spatial rate at which fertilisers have been applied | Free text e.g. 3kg/ha |
| manure_use | Response to application of manure on fields | Yes, No |
| manure_application_rate_monthly | Response to temporal rate at which manure has been applied to the field Monthly | Yes, No |
| manure_application_rate_every_six_months | Response to temporal rate at which manure has been applied to the field Every six months | Yes, No |
| manure_application_rate_yearly | Response to temporal rate at which manure has been applied to the field Yearly | Yes, No |
| manure_application_rate_every_two_years | Response to temporal rate at which manure has been applied to the field Every two years | Yes, No |
| manure_application_rate_other | Response to temporal rate at which manure has been applied to the field at other rates | Yes, No |
| At what rate has manure been applied? | Spatial rate at which the manure has been added to the field. | Free text e.g. 3kg/ha |
| pesticides__insecticides_use | The brand name of Pesticides/Insecticides used. | No; Yes, Free text of brand name provided by farmers  |
| fungicides_use | The brand name of Fungicides used. | No; Yes, Free text of brand name provided by farmers |
| herbicides_use | The brand name of Herbicides used. | No; Yes, Free text of brand name provided by farmers |
| tillage | Response for tillage method used on field | Yes, No |
| tillage_method | The method used to till the field | Reduced tillage, Direct drilling, Ploughed, Strip till drill, Primary Tilling |
| soil_texture | Description of the pysical texture of the soil | Sand, Loamy Sand, Sandy Loam, Loam, Silt Loam, Silt, Sandy Clay Loam, Clay Loam, Silty Clay Loam, Sandy Clay, Silty Clay, Clay |
| soil_ph	| Alkalinity or acidity of soil	| 1, 2, 3… 14 |
| available_p	| Concentration of  Phosphorus	| TBD |
| available_k	| Concentration of Potassium |	TBD |
| available_mg	| Concentration of Magnesium |	TBD |
| available_ca	| Concentration of Calcium |	TBD |
| available_na	| Concentration of Sodium |	TBD |
| extractable_cu	| Concentration of Copper	| TBD |
| extractable_zn	| Concentration of Zinc |	TBD |
| extractable_fe |	Concentration of Iron |	TBD |
| extractable_so4 |	Concentration of Sulphates |	TBD |
| extractable_mo	| Concentration of Molybdium	| TBD |
| extractable_mn	| Concentration of Manganese |	TBD |
| extractable_co | Concentration of Cobalt | TBD |
| Any other relevant info you'd like to tell us? | Response for additional information | Yes, No |
| Please add any relevant information | Free text of additional information provided by farmers | Free text of additional information provided by farmers |
| Is there any other information about your field that you would like to tell us? | Response for additional information | Yes, No |
| Please add any relevant information | Free text of additional information provided by farmers | Free text of additional information provided by farmers |
| We may need to contact you for further information if needed. Are you happy for us to do this? | Response for contact | Yes, No |
| What is your preferred method of contact? | Response for contact method preference | Email, Phone |
| What is your email address? | Response for contact method preference | Free text of additional information provided by farmers |
| What is your phone number? | Response for contact method preference | Free text of additional information provided by farmers |
