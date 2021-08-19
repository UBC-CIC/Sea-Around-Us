# web_data_layer



Catch data layers: Field names and webpages may refer to data layers, that corresponds to the triplets (where, from whom, what) related to each catch, so Catch data layers may be preferable to use.

Note: there are other types of layers, but sometimes they are referred to as layers only. Caution is required in these cases to which layer it is referring to.

| Column  name  | Data  type | Description  / Comment      |
| ------------- | ---------- | --------------------------- |
| data_layer_id | smallint   | Catch data layer identifier |
| name          | string     | Catch data layer name       |



### Values

Catch data layers:

| ID   | Name                         | Description                                                  |
| ---- | ---------------------------- | ------------------------------------------------------------ |
| 1    | Reconstructed domestic catch | Catch taken by a fishing country in its own EEZ, also called domestic catch or ‘Layer 1’ |
| 2    | Inferred foreign catch       | Catch by each fishing country in other EEZs and/or the high seas, also called foreign catch or ‘Layer 2’ |
| 3    | Assigned Tuna RFMO catch     | Catch of all tuna and large pelagic species caught by each fishing country’s industrial fleet, also called tuna blocks or ‘Layer 3’ |



See definition in this page http://www.seaaroundus.org/catch-reconstruction-and-allocation-methods/
in subsection 4.1.

