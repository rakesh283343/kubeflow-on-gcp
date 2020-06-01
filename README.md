# kubeflow-on-gcp
Deploy Kubeflow on GCP Free Account 

### Setup your Google Cloud Account

#### Step 1: Loging to google cloud for authorization
```bash
gcloud auth login

# create application default credentials
gcloud auth application-default login 
```
#### Step 2: Set the working gcp project and zone as default
```bash
# Set as environement variables as well, we will need this in the next steps

export PROJECT=<YOUR_PROJECT_ID>
export ZONE=<SET_YOUR_ZONE>

gcloud config set project ${PROJECT}
gcloud config set compute/zone ${ZONE}
```
### Prepare Kubeflow
#### Step 1: Download and extract kubeflow release based on your OS 
You can find the latest release here https://github.com/kubeflow/kfctl/releases

```bash
# Set the link as env variable as well as the file name

export KFCTL_FILE_PATH=https://github.com/kubeflow/kfctl/releases/download/v1.0.1/kfctl_v1.0.1-0-gf3edb9b_linux.tar.gz
export KFCTL_FILE="kfctl.tar.gz"

# Download kfctl
wget $KFCTL_FILE_PATH -O $KFCTL_FILE

```

