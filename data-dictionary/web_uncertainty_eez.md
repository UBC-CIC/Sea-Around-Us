# web_uncertainty_eez



Reliability of the catch allocation for EEZ, by fishery sector, catch data layer, and period.

Note: the fields and some SAU webpages refer to ‘uncertainty’ but ‘reliability’ is a better wording that will used from now on.

Computed as the weighted mean of catch amount and scores.

| Column  name   | Data  type | Description  / Comment                                     |
| -------------- | ---------- | ---------------------------------------------------------- |
| eez_id         | int        | Foreign key to table web_eez                               |
| sector_type_id | smallint   | Foreign key to table web_sector_type                       |
| period_id      | smallint   | Foreign key to table web_uncertainty_time_period           |
| score          | smallint   | Reliability score of the catch allocation by EEZ by period |
| layer          | smallint   | Foreign key to table web_data_layer                        |



### Values

Scores: decimal between 1: unreliable and 4: reliable

See definitions in http://www.seaaroundus.org/catch-reconstruction-and-allocation-methods/
in subsection Step 7 of Section 1.

