# PyConIndia2016Demos
## This Repo contains Jupyter Notebook and the Azure ML experiment.

## To run the Notebook on local machine
* Clone or Download the repo.
* Install Anaconda https://docs.continuum.io/anaconda/install
* Once the installation is done, open command prompt, go to the directory where .ipynb file is located and run the command Jupyter notebook
* Run the notebook

## To run the Notebook in Azure ML studio
* Clone or Download the repo.
* Open Azure machine learning studio https://azure.microsoft.com/en-us/services/machine-learning/
* Go to New -> Dataset -> Upload the data file
* Go to New -> Notebooks -> Upload and Select the .ipynb file in the Repo
* Once the file is uploades, open the notebook.
* Once the notebook opens replace following code 
   df = pd.read_csv("pima-data.csv") # Load data

to

  from azureml import Workspace
  ws = Workspace()
  ds = ws.datasets['pima-data.csv']
  df = ds.to_dataframe()

 
## Azure ML Experiment 
* Open Azure Machine learning studio.
* Create Azure experiment as shown in the Screenshot.

