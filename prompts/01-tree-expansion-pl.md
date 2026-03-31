# Tree Expansion, Poland First

Push every branch of your family tree as far back as possible using Polish and Poland related genealogical records first, then broader web research only when necessary.

## Autoresearch Configuration

**Goal**: For every ancestor currently in `[VAULT_PATH]/Family_Tree.md` who is Polish, Poland adjacent, or plausibly from former Polish territories, search for parents, siblings, spouses' families, and additional generations. Update the vault after each verified discovery. Keep iterating until no more supported ancestors can be found through free or accessible web sources.

**Metric**: Number of new ancestors or individuals added to `Family_Tree.md`

**Direction**: Maximize

**Verify**: Count the number of named individuals in `Family_Tree.md` before and after each iteration. Log the delta.

**Guard**:
- Do not fabricate ancestors.
- Every addition must cite a source.
- Do not trust user contributed trees, including Geni, Ancestry hints, WikiTree, and MyHeritage, without corroboration from at least one independent source.
- Do not modify existing dates or names during expansion unless a source clearly shows the existing version is incomplete and the new version is being added as a documented variant.
- Preserve all observed name variants instead of collapsing them into one guessed spelling.
- Mark any unverified additions with `(unverified)` in the tree.
- Treat surname maps and modern surname distributions as clues, not proof of lineage.
- Do not assume two people are the same person just because the surname and year roughly match.

**Iterations**: 8

**Protocol**:

1. **Baseline**
   - Read `[VAULT_PATH]/Family_Tree.md` completely.
   - Count every named individual.
   - Record this baseline in `[VAULT_PATH]/Research_Log.md`.

2. **Identify Polish expansion targets**
   - For each leaf node, or each person with missing parents, note:
     - Full recorded name
     - All known name variants
     - Dates or estimated year ranges
     - Village, parish, town, powiat, voivodeship, partition, or country clues
     - Religion, if known
     - Migration clues, including US naturalization, ship manifests, obituaries, and death records
   - Prioritize:
     - People with a specific locality
     - People with both date range and locality
     - People whose line is shallowest
     - Women whose maiden names are known
     - Immigrants with post-1906 US naturalization records or specific birthplace clues

3. **Normalize names before searching**
   - Generate and log plausible search variants for each target:
     - Diacritic and non-diacritic forms
     - Masculine and feminine surname forms where relevant, including `-ski/-ska`
     - Anglicized or emigrant spellings
     - Przydomek or `vulgo` forms if present
     - Reversed order or multi-part surname forms if found in records
   - Preserve every variant used in the research log.

4. **Resolve locality before broad expansion**
   - For each target, try to identify the most precise place possible:
     - Village
     - Parish
     - Gmina
     - Powiat
     - Voivodeship
     - Historical partition, Russian, Prussian, or Austrian, if relevant
   - Use immigration, census, obituary, military, and church clues to narrow the place.
   - If locality is ambiguous, log all plausible candidates and rank them.

5. **Search strategy per ancestor, Poland first**
   - Run searches in this order:

   a. **Geneteka style search**
   - Search by surname variants across relevant regions first
   - If surname is common, narrow by parish, spouse, event type, or year range
   - Look for clustered baptisms, marriages, deaths, and siblings in the same locality

   b. **Polish archive search**
   - Search for the parish or civil registration unit in Polish state archives
   - Look for record groups covering the correct years and event types
   - Prefer original record images or archive level descriptions over copied tree data

   c. **Scanned register search**
   - Search available parish register scans and image collections for the exact locality and year range
   - If a likely baptism or marriage is found, extract parents, witnesses, godparents, house numbers, and occupation details

   d. **Region specific search**
   - If the locality is in Galicia or another borderland region, check region specific resources
   - If the line may be from former eastern territories, consider cross border archives and multilingual record systems

   e. **Migration back-linking**
   - If the Polish locality is still unclear, search immigration, naturalization, obituary, cemetery, and church records in the destination country for exact birthplace clues
   - Use these records to return to the Polish locality search

   f. **Broad web search only after the above**
   - Use broader web search only when Poland first records fail
   - Treat user trees and compiled genealogies as leads only

6. **Evaluate results**
   - For each search hit, ask:
     - Does the name match, allowing for documented variants
     - Do dates align within a plausible range
     - Does locality align at the village, parish, or district level
     - Does the relationship make sense given the record type
     - Is the source primary, secondary, or tertiary
   - Strongly prefer:
     - Vital records
     - Church registers
     - Original archive images
     - Contemporary civil records
   - If using a secondary source, require at least one independent corroborating source before adding new parents or generations.

7. **Use collateral research**
   - Search siblings, witnesses, godparents, neighbors, and spouses' families when direct parent evidence is missing.
   - Pay attention to:
     - Repeated house numbers
     - Recurring given names
     - Witnesses at marriages
     - Godparents in baptisms
     - Occupation and status markers
   - Use collateral lines to confirm family clusters, not to invent links.

8. **Handle Polish naming correctly**
   - Preserve original record forms where possible.
   - Note surname gender differences and emigrant spelling shifts.
   - Record przydomki separately when present.
   - Do not discard a match solely because the record uses a variant form of the surname.

9. **Update the vault**
   - For each confirmed new ancestor or relative:
     - Add them to `Family_Tree.md` in the correct position
     - If sufficient data exists, create a person file using `[VAULT_PATH]/templates/person.md`
     - Record all relevant name variants in the person file
     - Note locality metadata as precisely as possible
     - Add the source to the person file's Document Sources section

10. **Log the search**
   - In `[VAULT_PATH]/Research_Log.md`, record:
     - Date and search target
     - Name variants used
     - Locality candidates considered
     - Queries used
     - Sources searched
     - Results, positive or negative
     - New individuals added
     - Remaining ambiguities
     - Confidence level for each newly asserted relationship

11. **Update the count**
   - Recount named individuals in `Family_Tree.md`
   - Report the delta
   - Note which branch produced the gain

12. **Repeat**
   - Move to the next best target.
   - Prioritize:
     - Branches with exact locality clues
     - Branches with recent immigrant documentation
     - Branches where one confirmed Polish record can unlock multiple relatives
     - Branches where sibling clustering suggests a recoverable family group

## Tips

- Polish records may appear in Polish, Latin, Russian, or German depending on time and partition.
- A surname alone is not enough. Locality is often more important than surname.
- Common surnames require parish level narrowing.
- Women may appear under maiden name, married name, or historically gendered surname forms.
- Przydomki can distinguish unrelated families sharing the same base surname.
- Negative results matter. Log them.
- If two sources conflict, prefer the higher quality source and document the discrepancy rather than silently choosing.