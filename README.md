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

# Extract the content while downlad finished
tar -xvf ${KFCTL_FILE}
```
#### Step 2: Add KFCTL to env PATH
```bash
PATH=${PATH}:$(pwd)
```
### Setup Deployment
#### Step 1: Get Client ID and Client Secret from Google Cloud 
![Screenshot](api_service_credentials.png)

- Create an <h4> Create OAuth client ID </h4>
- Choose Application type as <h4> Web Application </h4>
- Rename an application name wathever you want
- Add URI by following the pattern: <h4> https://iap.googleapis.com/v1/oauth/clientIds/<CLIENT_ID>:handleRedirect </h4>
  
  RQ: To get CLIENT_ID first create the OAuth Client without URI and then edit it to add URI
 



