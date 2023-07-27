# Install PySpark usign Anaconda

Install Anaconda, if you haven’t already

Run Anaconda Prompt Administrator

Create a new conda environment `conda create -n pyspark_env python=3.9` 

The new conda environment is called `pyspark_env` in this example.

Activate the new environment `conda activate pyspark_env`

Install java `conda install openjdk`

Install pyspark `conda install pyspark`

Install findspark `conda install -c conda-forge findspark`

Install jupyter `conda install jupyter`

Run pyspark `pyspark` to check installation went well.

If PySpark runs, you're good to go.

If you get an error about python not being found, run the following:

- Get the location of python inside your environment `where python` (Windows), `which python` (Mac & Linux)
- Persist the `PYSPARK_PYTHON` environment variable as the output of `where python` by running `conda env config vars set PYSPARK_PYTHON=C:\ProgramData\anaconda3\envs\pyspark_env\python.exe` Note that your `C:\` path might be slightly different.
- Deactivate the conda environment `conda deactivate`
- Activate it again `conda activate pyspark_env`
- run pyspark again `pyspark`

To run pyspark inside of a Jupyter Notebook, launch Jupyter from inside your pyspark_env environment `jupyter notebook`

