1. Check for certain String (e.g. 'rna' in Column 1)
   
   ```
   df.loc[df.column_1.str.contains('rna_*')]
   ```
