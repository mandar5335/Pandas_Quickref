* [Pandas Tricks](#pandas_tricks)
* [Conda Tricks](#conda_tricks)

## pandas_tricks
1. Check for certain String (e.g. 'rna' in Column 1)
   
   ```
   df.loc[df.column_1.str.contains('rna_*')]
   ```
2. Sort entries by property_1 (e.g. docking score) but groupby property_2 (e.g. ligand_title)
   ```
   result = df.loc[df.groupby("LIG_TITLE")["docking_score"].idxmin()]
   idxmin = index of minimum docking score
   ```

  ## conda_tricks:
1. Export environment without Prefix:
     ```
     conda env export | grep -v "^prefix: " > environment.yml
     ```
2. Create environment from `environment.yml`:
   ```
   conda env create -f environment.yml
   ```
3. Change the Default Browser to Google Chrome for Jupyter Notebooks in OS X
   ```
   jupyter notebook --generate-config
   ```
   *open ~/.jupyter/jupyter_notebook_config.py with text editor* and 
   __add these lines__
   ```
   # import webbrowser
   c.NotebookApp.browser = u'open -a /Applications/Google\ Chrome.app %s'
   ```
