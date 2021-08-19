# web_fishing_entity




Fishing entities: Geo-administrative entities under which Sea Around Us gathers catches administratively from all fishing ‘areas’ (as catch data layers) exploited by the fishing entity: it may be countries, country mainland only, country states/provinces, territories (usually overseas, usually islands, but not exclusively). The list has been established by SAU.


| Column  name                          | Data  type | Description  / Comment                         |
| ------------------------------------- | ---------- | ---------------------------------------------- |
| fishing_entity_id                     | smallint   | Fishing entity identifier                      |
| name                                  | string     | Fishing entity name                            |
| geo_entity_id                         | int        | Foreign key into the geographic module         |
| date_allowed_to_fish_other_eezs       | int        | First year fishing in non-domestic EEZs        |
| date_allowed_to_fish_high_seas        | int        | First year fishing in high seas                |
| legacy_c_number                       | int        | Legacy field: not used                         |
| is_currently_used_for_web             | boolean    | If fishing entity used in the web pages        |
| is_currently_used_for_reconstruction  | boolean    | If fishing entity used in reconstruction phase |
| is_allowed_to_fish_pre_eez_by_default | boolean    | Fishing in non-domestic EEZs before EEZs exist |
| remarks                               | string     | Any comment                                    |



