1. Check for certain String (e.g. 'rna' in Column 1)
   
   ```
   df.loc[df.column_1.str.contains('rna_*')]
   ```
2. Sort entries by property_1 (e.g. docking score) but groupby property_2 (e.g. ligand_title)
   ```
   result = df.loc[df.groupby("LIG_TITLE")["docking_score"].idxmin()]
   idxmin = index of minimum docking score
   ```
