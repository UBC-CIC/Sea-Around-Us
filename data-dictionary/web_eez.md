# web_eez



EEZ: Exclusive Economic Zone; defined by the UN Law of the Sea (UNCLOS), cover the area from the coast to 200 nautical miles off the coast; rules applied when theoretical areas overlap; some areas are claimed by several countries.

| Column  name                           | Data  type | Description  / Comment                              |
| -------------------------------------- | ---------- | --------------------------------------------------- |
| eez_id                                 | int        | EEZ identifier                                      |
| name                                   | string     | EEZ name                                            |
| alternate_name                         | string     | EEZ other name                                      |
| geo_entity_id                          | int        | Foreign key into the geographic module              |
| area_status_id                         | int        | Internal field: not to be used                      |
| legacy_c_number                        | int        | Legacy field: not used                              |
| legacy_count_code                      | string     | Legacy field: not used                              |
| fishbase_id                            | string     | Foreign key to FishBase.COUNTRYREF (1)              |
| coords                                 | string     | Legacy field: not used                              |
| can_be_displayed_on_web                | boolean    | If the EEZ is ready to be used on the web           |
| is_currently_used_for_web              | boolean    | If the EEZ is actually used on the web              |
| is_currently_used_for_reconstruction   | boolean    | If the EEZ is actually used for reconstruction      |
| declaration_year                       | int        | Year of the creation of the EEZ                     |
| earliest_access_agreement_date         | int        | 1st year of fishing agreement with foreign country  |
| is_home_eez_of_fishing_entity_id       | smallint   | Foreign key to fishing_entity if sovereign of EEZ   |
| allows_coastal_fishing_for_layer2_data | boolean    | If foreign fishing authorized in coastal waters     |
| ohi_link                               | string     | Deep link to the Ocean Health Index (2)             |
| is_retired                             | boolean    | If the EEZ does not exist anymore, e.g. Yugoslavia  |
| gsi_link                               | string     | Deep link to the Global Slavery Index (3)           |
| issf_link                              | string     | Link to the Inf. Syst. on Small-scale Fisheries (4) |
| hdi_link                               | string     | Deep link to Human Development Index (5)            |
| iso_3                                  | string     | ISO 3alpha country code                             |
| iso_2                                  | string     | ISO 2alpha country code                             |
| hdi                                    | string     | Human Development Index value                       |
| hdi_source                             | string     | Human Development Index source of value             |
| hdi_publication_year                   | int        | Human Development Index publication year of value   |



(1)	Countries (not EEZ!) in FishBase mean territories: country, country mainland, oversea territories, islands. This list has been established by FishBase.
(2)	OHI: Ocean Health Index at http://www.oceanhealthindex.org/
(3)	GSI: Global Slavery Index at https://www.globalslaveryindex.org/
(4)	ISSF: Information System on Small-scale Fisheries at https://issfcloud.toobigtoignore.net/
(5)	HDI: Human Development Index at http://hdr.undp.org/



### Values

See values in appendix.

