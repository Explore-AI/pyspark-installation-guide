# Installing PySpark using Anaconda

## 1. Download and Install Anaconda

Go to https://anaconda.com/ and select Anaconda Individual Edition to download the Anaconda and install, for windows you download the `.exe` file and for Mac download the `.pkg` file.

<p align="center">
    <img src="https://assets.anaconda.com/production/anaconda-meta.jpg?w=1200&h=630&q=82&auto=format&fit=clip&dm=1632326952&s=2b336a00fa13405f84ce2f5b74e21fee" alt="Alt text" width="600">
</p>

## 2. Create a virtual environment

- The command below will create a virtual environment named "pyspark_env" with python

```bash
conda create -n pyspark_env
```

- The following command will activate the virtual environment

```bash
conda activate pyspark_env
```

## 3. Install Java

PySpark uses Java underlying hence you need to have Java on your Windows or Mac.

```bash
conda install openjdk
```

## 4. Install PySpark

Use the following command to install PySpark. Note that there will be addtional packages that will be installed.

```bash
conda install pyspark
```

## 5. Install FindSpark

FindSpark is a library that helps you to find the location of the PySpark library.

```bash
conda install -c conda-forge findspark
```

## 6. Validate PySpark Installation

- The following command will launch the PySpark shell where you can write PySpark programs interactively:

```bash
pyspark
```

Create a PySpark DataFrame with some sample data to validate the installation. Enter the following commands in the PySpark shell in the same order. Note that SparkSession `spark` and SparkContext `sc` is by default available in PySpark shell.

<p align="center">
    <img src="https://sparkbyexamples.com/wp-content/uploads/2022/02/pyspark-example.png?ezimgfmt=rs:702x233/rscb1/ng:webp/ngcb1" alt="Alt text" width="800">
</p>

## 7. Install Jupyter Notebooks

- The following command will install Jupyter Notebooks

```bash
pip install jupyter
```

- To run Jupyter Notebooks use the following command:

```bash
jupyter notebook
```
