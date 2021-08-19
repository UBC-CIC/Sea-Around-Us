# web_cube_dim_taxon



Taxa: A taxon (plural taxa) is a taxonomic group of species at any level as part of the classification of species: species, genus (plural genera), family, order, class, phylum (plural phyla), kingdom. There can be intermediary rank like superclass, suborder, etc.



| Column  name        | Data  type | Description  / Comment                                       |
| ------------------- | ---------- | ------------------------------------------------------------ |
| taxon_key           | int        | Taxon identifier                                             |
| scientific_name     | string     | Current valid scientific name from FishBase or SeaLifeBase   |
| common_name         | string     | The English common name from FAO ASFIS Species List          |
| phylum              | string     | Phylum of the taxon / where the taxon is classed             |
| sub_phylum          | string     | Idem for subphylum                                           |
| super_class         | string     | Idem for superclass                                          |
| class               | string     | Idem for class                                               |
| super_order         | string     | Idem for superorder                                          |
| order               | string     | Idem for order                                               |
| suborder_infraorder | string     | Idem for suborder / infraorder (if infraorder then 2 names   |
| family              | string     | Idem for family                                              |
| genus               | string     | Idem for genus                                               |
| species             | string     | Idem for species                                             |
| comments_names      | string     | Any comments about the name, previous valid names, etc.      |
| is_retired          | boolean    | Indicates if the taxon is not in use anymore in the reconstruction (1) |
| taxon_group_id      | int        | Foreign key to table taxon_group                             |
| taxon_level_id      | int        | Taxonomic level/rank of the taxon                            |
| functional_group_id | smallint   | Foreign key to table functional_group                        |
| commercial_group_id | smallint   | Foreign key to table commercial_group                        |
| commercial          | smallint   | Legacy field: not used                                       |
| isscaap_id          | int        | ISSCAAP number of the taxon as defined by FAO                |
| cell_id             | int        | Legacy field: not used                                       |
| super_target        | smallint   | Legacy field: not used                                       |
| fb_spec_code        | int        | Foreign key to table FishBase.SPECIES                        |
| slb_spec_code       | int        | Foreign key to table SeaLifeBase.SPECIES                     |
| cla_code            | int        | SAU class identifier, also foreign key in FishBase.CLASSES   |
| ord_code            | int        | SAU order identifier, also foreign key in FishBase.ORDERS    |
| fam_code            | int        | SAU family identifier, also foreign key in FishBase.FAMILIES |
| gen_code            | int        | SAU genus identifier, also foreign key in FishBase.GENERA    |
| spe_code            | int        | SAU species identifier, also foreign key in FishBase.SPECIES |
| slb_cla_code        | int        | Foreign key to table SeaLifeBase.CLASSES                     |
| slb_ord_code        | int        | Foreign key to table SeaLifeBase.ORDERS                      |
| slb_fam_code        | int        | Foreign key to table SeaLifeBase.FAMILIES                    |
| slb_gen_code        | int        | Foreign key to table SeaLifeBase.GENERA                      |
| is_use              | boolean    | Legacy field: not used                                       |
| is_taxa_used        | boolean    | Field with uncertain status: not to be used                  |
| is_mariculture_only | boolean    | Indicates if the taxon is used in mariculture only (2)       |
| is_baltic_only      | boolean    | Indicates freshwater taxon catches to be included Baltic Sea (3) |
| sl_max              | double     | Maximum length, by default maximum standard length for fishes |
| slbl_max_type       | string     | Type of maximum length, by default SL for fishes             |
| sl_max_2            | double     | Experimental field: not to be used                           |
| comments_sl_max     | string     | Any comments about the maximum length                        |
| tl                  | double     | Trophic level from FishBase and SeaLifeBase estimations      |
| se_tl               | double     | Standard error of the trophic level                          |
| comments_tl         | string     | Any comments about the trophic level                         |
| lat_north           | int        | Northernmost latitude of the geographic distribution of the taxon |
| lat_south           | int        | Southernmost latitude of the geographic distribution of the taxon |
| min_depth           | int        | Depth range minimum taken/computed from FishBase or SeaLifeBase (3) |
| max_depth           | int        | Depth range maximum taken/computed from FishBase or SeaLifeBase (3,4) |
| loo                 | double     | Length infinity (also as Linf) of von Bertalanffy growth function (5) |
| woo                 | double     | Weight infinity (also as Winf) of von Bertalanffy growth function (5) |
| k                   | double     | Growth coefficient of von Bertalanffy growth function (5)    |
| a                   | double     | Y-axis intercept value of the length-weight relationship equation (6) |
| b                   | double     | Slope value of the length-weight relationship equation (6)   |
| comments_growth     | string     | Any comment about the growth                                 |
| has_habitat_index   | boolean    | If the taxon has a habitat index in the table taxon_habitat (7) |
| has_map             | boolean    | Indicates if the taxon has a geographic distribution map     |
| map_year            | smallint   | Year of the map computation                                  |
| vulnerability       | string     | Vulnerability of the taxon, from FishBase or SeaLifeBase     |
| resilience          | string     | Resilience of the taxon, from FishBase or SeaLifeBase        |
| updated_by          | string     | Who has last updated the record, and what.                   |
| date_updated        | string     | When the record was last modified (any field)                |
| lineage             | string     | The classification of the taxon from Phylum to Genus. (8)    |
| true_min_depth      | string     | Depth range minimum taken verbatim from FishBase or SeaLifeBase (9) |
| true_max_depth      | string     | Depth range minimum taken verbatim FishBase or SeaLifeBase (9) |



(1)	Retired taxon are kept to be able to check the past data.      
(2)	Some catches of these species are mistakenly reported with catch fishery statistics. This flag reminds the reconstruction team that these catches must not be included.      
(3)	The depth range is computed for supraspefic taxa (genus, family, and above, as the minimum of minima and maximum of maxima of the depth range of the species included in the taxon.      
(4)	CAUTION: for the pelagic taxa, the value is set as 9999 for the algorithm computing the distribution of the species. Refer to FishBase and SeaLifeBase to get the real value (also in field true_max_depth).     
(5)	Von Bertalanffy Growth Function (VGBF): Lt = Linf * (1 - exp(-K(t-t0)); t: age; Lt: Length at age t; Linf: asymptotic length (length at infinite age); K: growth coefficient; t0 is the theoretical age when lenght is zero.     
(6)	LWR: Length-weight relationship: W = a*L^b; W: Weight; L: Length.     
(7)	Used in the allocation process.     
(8)	Missing ranks are replaced by NA. This field has the type ltree in PostgreSQL and is use for recursive queries to compute the catch for a taxon, including all the children of the taxon.     
(9)	For species only.      

