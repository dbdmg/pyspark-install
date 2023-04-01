# PySpark Installation Guide
This guide was created for the students of the "Distributed architectures for big data processing and analytics" course at Politecnico di Torino.
**This guide must be used only in case you want to run your application without using the distributed cluster.**
**On the distributed cluster, everything is already configured and ready to run Spark application.**
**Please follow this guide only in case you want to execute applications on your own, without the distributed cluster.**

It will guide you on the installation of JupyterLab + PySpark.

Three options are available to run your code locally:
 - Google Colab
 - Your own computer
 - LABINF's computer


## Google Colab
** Requirement: you need a Google account to be able to use Google Colab. Internet connection is required to run the code. **
This is the easiest solution and it does not require any configuration.

### Configuration

Steps:
 - Go to the Colab's entry page ([link](https://colab.research.google.com/))
 - Create a new notebook
 - (optional) Verify that **no** Accellerator (GPU/TPU) is being used
    - Runtime -> Change runtime type -> Accelerator: None
 - Connect to a runtime by going into the top-right corner of the notebook and clicking `Connect`
 - After connection, Colab should report RAM and Disk usage
 - Install PySpark by running a cell with the following code: `!pip install pyspark`
 - Instantiate a SparkSession by running the following code in a cell:
```
from pyspark.sql import SparkSession

spark = SparkSession.builder.getOrCreate()
sc = spark.sparkContext
```

### Data upload
To upload sample files on Google Colab, you can either:
 - upload files from your laptop
 ![ColabUpload](images/colab_upload.png)
 - use the command line given the download link:
 ```
 !wget download_link
 ```

## Local Installation


## LABINF Installation