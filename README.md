# SoraVideoGenAnalysis
Research and capabilities analysis of the Sora model

## Overview
This repo shows various experiments for capability testing the OpenAI Sora models on Azure.  

## Setup
This project requires access to an [Azure OpenAI resource](https://portal.azure.com/#create/Microsoft.CognitiveServicesOpenAI) to run the Sora model.  At the [deployment page in Azure AI Foundry](https://ai.azure.com/resource/deployments), you will need to deploy the **sora** model.  Then copy the .env.template file into a new file called .env, and update the .env file with the endpoint (and the deployment name if you change from the default).  You will also need to supply either an API key or use Microsoft Entra ID (formerly called Azure Active Directory) authentication.  We strongly recommend Microsoft Entra ID authentication for greater security.  To set it up, see https://learn.microsoft.com/azure/ai-services/openai/how-to/managed-identity.  Don't forget that you may need to run "az login" to refresh your credentials.  

Finally, use the following commands in a python environment (such as an Anaconda prompt window) to set up your environment.  This creates and activates an environment and installs the required packages.  For subsequent runs after the initial install, you will only need to activate the environment and then run the python script.  

### First run
```
conda create --name soraAnalysis -y
conda activate soraAnalysis

pip install -r requirements.txt
jupyter notebook soraAnalysis.ipynb
```

### Subsequent runs
```
conda activate soraAnalysis
jupyter notebook soraAnalysis.ipynb
```
