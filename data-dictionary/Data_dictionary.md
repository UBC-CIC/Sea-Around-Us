# Data Dictionary



## web_rfmo

| Column  name | Data  type | Description  / Comment |
| ------------ | ---------- | ---------------------- |
| rfmo_id      | int        |                        |
| name         | string     |                        |
| long_name    | string     |                        |
| profile_url  | string     |                        |



## web_uncertainty_eez

| Column  name   | Data  type | Description  / Comment |
| -------------- | ---------- | ---------------------- |
| eez_id         | int        |                        |
| sector_type_id | smallint   |                        |
| period_id      | smallint   |                        |
| score          | smallint   |                        |
| layer          | smallint   |                        |

## web_sector_type

| Column  name   | Data  type | Description  / Comment |
| -------------- | ---------- | ---------------------- |
| sector_type_id | smallint   |                        |
| name           | string     |                        |

## web_gear

| Column  name | Data  type | Description  / Comment |
| ------------ | ---------- | ---------------------- |
| gear_id      | smallint   |                        |
| name         | string     |                        |
| super_code   | string     |                        |
| notes        | string     |                        |

## web_functional_groups

| Column  name                         | Data  type | Description  / Comment |
| ------------------------------------ | ---------- | ---------------------- |
| functional_group_id                  | smallint   |                        |
| target_grp                           | int        |                        |
| name                                 | string     |                        |
| description                          | string     |                        |
| include_in_depth_adjustment_function | boolean    |                        |
| size_range                           | string     |                        |
| fgi_block                            | string     |                        |

## web_fishing_entity

| Column  name                          | Data  type | Description  / Comment |
| ------------------------------------- | ---------- | ---------------------- |
| fishing_entity_id                     | smallint   |                        |
| name                                  | string     |                        |
| geo_entity_id                         | int        |                        |
| date_allowed_to_fish_other_eezs       | int        |                        |
| date_allowed_to_fish_high_seas        | int        |                        |
| legacy_c_number                       | int        |                        |
| is_currently_used_for_web             | boolean    |                        |
| is_currently_used_for_reconstruction  | boolean    |                        |
| is_allowed_to_fish_pre_eez_by_default | boolean    |                        |
| remarks                               | string     |                        |

## web_cube_dim_taxon

| Column  name        | Data  type | Description  / Comment |
| ------------------- | ---------- | ---------------------- |
| taxon_key           | int        |                        |
| scientific_name     | string     |                        |
| common_name         | string     |                        |
| phylum              | string     |                        |
| sub_phylum          | string     |                        |
| super_class         | string     |                        |
| class               | string     |                        |
| super_order         | string     |                        |
| order               | string     |                        |
| suborder_infraorder | string     |                        |
| family              | string     |                        |
| genus               | string     |                        |
| species             | string     |                        |
| comments_names      | string     |                        |
| is_retired          | boolean    |                        |
| taxon_group_id      | int        |                        |
| taxon_level_id      | int        |                        |
| functional_group_id | smallint   |                        |
| commercial_group_id | smallint   |                        |
| commercial          | smallint   |                        |
| isscaap_id          | int        |                        |
| cell_id             | int        |                        |
| super_target        | smallint   |                        |
| fb_spec_code        | int        |                        |
| slb_spec_code       | int        |                        |
| cla_code            | int        |                        |
| ord_code            | int        |                        |
| fam_code            | int        |                        |
| gen_code            | int        |                        |
| spe_code            | int        |                        |
| slb_cla_code        | int        |                        |
| slb_ord_code        | int        |                        |
| slb_fam_code        | int        |                        |
| slb_gen_code        | int        |                        |
| is_use              | boolean    |                        |
| is_taxa_used        | boolean    |                        |
| is_mariculture_only | boolean    |                        |
| is_baltic_only      | boolean    |                        |
| sl_max              | double     |                        |
| slbl_max_type       | string     |                        |
| sl_max_2            | double     |                        |
| comments_sl_max     | string     |                        |
| tl                  | double     |                        |
| se_tl               | double     |                        |
| comments_tl         | string     |                        |
| lat_north           | int        |                        |
| lat_south           | int        |                        |
| min_depth           | int        |                        |
| max_depth           | int        |                        |
| loo                 | double     |                        |
| woo                 | double     |                        |
| k                   | double     |                        |
| a                   | double     |                        |
| b                   | double     |                        |
| comments_growth     | string     |                        |
| has_habitat_index   | boolean    |                        |
| has_map             | boolean    |                        |
| map_year            | smallint   |                        |
| vulnerability       | string     |                        |
| resilience          | string     |                        |
| updated_by          | string     |                        |
| date_updated        | string     |                        |
| lineage             | string     |                        |
| true_min_depth      | string     |                        |
| true_max_depth      | string     |                        |

## web_data_layer

| Column  name  | Data  type | Description  / Comment |
| ------------- | ---------- | ---------------------- |
| data_layer_id | smallint   |                        |
| name          | string     |                        |

## web_uncertainty_time_period

| Column  name | Data  type | Description  / Comment |
| ------------ | ---------- | ---------------------- |
| period_id    | smallint   |                        |
| year_range   | string     |                        |

## web_commercial_groups

| Column  name        | Data  type | Description  / Comment |
| ------------------- | ---------- | ---------------------- |
| commercial_group_id | smallint   |                        |
| name                | string     |                        |

## web_eez

| Column  name                           | Data  type | Description  / Comment |
| -------------------------------------- | ---------- | ---------------------- |
| eez_id                                 | int        |                        |
| name                                   | string     |                        |
| alternate_name                         | string     |                        |
| geo_entity_id                          | int        |                        |
| area_status_id                         | int        |                        |
| legacy_c_number                        | int        |                        |
| legacy_count_code                      | string     |                        |
| fishbase_id                            | string     |                        |
| coords                                 | string     |                        |
| can_be_displayed_on_web                | boolean    |                        |
| is_currently_used_for_web              | boolean    |                        |
| is_currently_used_for_reconstruction   | boolean    |                        |
| declaration_year                       | int        |                        |
| earliest_access_agreement_date         | int        |                        |
| is_home_eez_of_fishing_entity_id       | smallint   |                        |
| allows_coastal_fishing_for_layer2_data | boolean    |                        |
| ohi_link                               | string     |                        |
| is_retired                             | boolean    |                        |
| gsi_link                               | string     |                        |
| issf_link                              | string     |                        |
| hdi_link                               | string     |                        |
| iso_3                                  | string     |                        |
| iso_2                                  | string     |                        |
| hdi                                    | string     |                        |
| hdi_source                             | string     |                        |
| hdi_publication_year                   | int        |                        |

## web_v_fact_data

| Column  name                | Data  type | Description  / Comment |
| --------------------------- | ---------- | ---------------------- |
| area_data_key               | int        |                        |
| taxon_key                   | int        |                        |
| fishing_entity_id           | smallint   |                        |
| gear_id                     | int        |                        |
| time_key                    | int        |                        |
| year                        | int        |                        |
| area_key                    | int        |                        |
| main_area_id                | int        |                        |
| sub_area_id                 | int        |                        |
| data_layer_id               | smallint   |                        |
| marine_layer_id             | int        |                        |
| catch_type_id               | smallint   |                        |
| catch_status                | string     |                        |
| reporting_status_id         | smallint   |                        |
| reporting_status            | string     |                        |
| sector_type_id              | smallint   |                        |
| end_use_type_id             | int        |                        |
| score                       | int        |                        |
| catch_sum                   | string     |                        |
| real_value                  | double     |                        |
| primary_production_required | double     |                        |
| catch_trophic_level         | string     |                        |
| catch_max_length            | string     |                        |
