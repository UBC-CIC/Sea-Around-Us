# web_v_fact_data



Catch weight by various dimensions.

| Column  name                | Data  type | Description  / Comment                                       |
| --------------------------- | ---------- | ------------------------------------------------------------ |
| area_data_key               | int        | Auto-generated identifier of the record                      |
| taxon_key                   | int        | Foreign key to table web_taxon                               |
| fishing_entity_id           | smallint   | Foreign key to table web_fishing_entity                      |
| gear_id                     | int        | Foreign key to table web_gear                                |
| time_key                    | int        | Year index = Year - 1950                                     |
| year                        | int        | Year of the catch                                            |
| area_key                    | int        | Foreign key to the table web_area (1)                        |
| main_area_id                | int        | Foreign key to a table dependent of the marine layer (2)     |
| sub_area_id                 | int        | Foreign key to an area in another marine layer (3)           |
| data_layer_id               | smallint   | Foreign key to table data_layer                              |
| marine_layer_id             | int        | Foreign key to table marine_layer                            |
| catch_type_id               | smallint   | Foreign key to table catch_type                              |
| catch_status                | string     | Catch type abbreviation (4)                                  |
| reporting_status_id         | smallint   | Foreign key to table reporting_status (4)                    |
| reporting_status            | string     | Reporting status name (abbreviation)                         |
| sector_type_id              | smallint   | Foreign key to table sector_type                             |
| end_use_type_id             | int        | Foreign key to table end_use                                 |
| score                       | int        | Reliability score of the catch                               |
| catch_sum                   | string     | Weight of the catch in metric tons                           |
| real_value                  | double     | Ex-vessel financial value of the catch (5)                   |
| primary_production_required | double     | Primary production necessary to produce the catch amount (6) |
| catch_trophic_level         | string     | Trophic level of the taxon                                   |
| catch_max_length            | string     | Maximum standard length of the taxon                         |



(1)	Area as intersection of the main area and the subarea.
(2)	Example, if marine layer = 1, then main_area_if is the foreign key to table web_EEZ, 
(3)	Depends on the marine layer.
(4)	Note that the field names are different: Catch_*type*_id and catch_*status*.
(5)	Price that fishermen get (not the price that client pay in fish store).
(6)	Catch must be understood as the caught biomass in that context.



### Values

Scores: decimal between 1: unreliable and 4: reliable

See definitions in http://www.seaaroundus.org/catch-reconstruction-and-allocation-methods/
in subsection Step 7 of Section 1.

