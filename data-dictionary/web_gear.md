# web_gear



Fishing gears: Operated by fisheries to catch organisms.

They are organized in three levels:
-	The fishing gears gathered in higher categories, the fishing gear types, that are represented by the field super_code (note: it is not actually a code but a generic fishing gear name, see values).
-	The basis of records is the fishing gear (identified by gear_id);
-	Some of these gears encompass themselves several fishing gears that are not detailed.

*** CAREFUL ***
Some fishing gear names and fishing gear type names are the same, e.g., bottom trawl. In the catch data, only the gear names (gear_id) are indicated. On the graphs on the web, sometimes the super_codes are used to aggregate data by fishing gear type, but they are called ‘gear’ only, which may be confusing.

| Column  name | Data  type | Description  / Comment                                |
| ------------ | ---------- | ----------------------------------------------------- |
| gear_id      | smallint   | Fishing gear identifier                               |
| name         | string     | Fishing gear name                                     |
| super_code   | string     | Type of fishing gear name                             |
| notes        | string     | Detailed description of the fishing gears encompassed |



### Values

Super_code = Type of fishing gear

| Value         | List of individual gears encompassed in the type of gear     |
| ------------- | ------------------------------------------------------------ |
| bottom trawl  | bottom trawl, beam trawl, otter trawl, shrimp trawl          |
| gillnets      | gillnet, trammel nets                                        |
| longline      | longline, pole and line, hand lines, lines                   |
| other         | dragged gear, dredge, hand or tools, pots or traps, mixed gear, other nets, other |
| pelagic trawl | pelagic trawl                                                |
| purse seine   | purse seine, encircling nets                                 |
| small scale   | artisanal fishing gear, recreational fishing gear, subsistence fishing gear, |
|               | cast nets, bagnets, harpoon, hand or tools, small scale seine nets, |
|               | small scale encircling nets, small scale trammel net, small scale gillnets, |
|               | small scale other nets, small scale pots or traps, small scale lines, |
|               | small scale hand lines, small scale pole lines, small scale longline, |
|               | small scale purse seine, other industrial                    |
| unknown       | unknown class, unknown by source, unknown by author          |

See further explanations http://www.seaaroundus.org/catch-reconstruction-and-allocation-methods/
in subsection Step 2 of Section 1.

