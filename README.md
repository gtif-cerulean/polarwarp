# polarwarp
Polar Warp repository including code, description and resources

This workflow processes Sentinel-1 satellite data with sea ice forecasting using Copernicus Marine Service data and DESP (Destination Earth) platform.


## Prerequisites

- Kubernetes cluster with Argo Workflows
Access to:
- Copernicus Marine Service account
- DESP (Destination Earth) platform account

## Quick Setup
### 1. Clone the repository

### 2.Update Environment-Specific Settings
Edit workflow.yaml and change:


**Change namespace**
namespace: your-namespace

**Update/remove storage class (or use "standard")**
storageClassName: your-storage-class  # or remove this line

**Update/remove service account**
serviceAccountName: your-service-account  # or remove this line


### 3. use credentials for the services

Option A

- set credentials as secrets on kubernetes level and adapt names in the workflow

Option B

- use credentials directly in the workflow and just delete the env variable section from workflow yaml and replace variables with actual values
