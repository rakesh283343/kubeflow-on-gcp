# kubeflow-on-gcp
Deploy Kubeflow on GCP Free Account 

This repo guides you how to deploy and explore kubeflow without paying on GCP 
### Setuo your Google Coud Account

#### Step 1: Loging to google cloud for authorization
```bash
gcloud auth login
```
#### Step 2: Set the working gcp project and zone as default
```bash
# Set as environement variables as well, we will need this in the next steps

export PROJECT=<YOUR_PROJECT_ID>
export ZONE=<SET_YOUR_ZONE>

gcloud config set project ${PROJECT}
gcloud config set compute/zone ${ZONE}
s
```
