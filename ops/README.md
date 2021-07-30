**OPS PIPELINE**

GCP Services used:
- deploymentmanager.googleapis.com
- sourcerepo.googleapis.com

Mirror your GitLab repo to Source repo by following this guide:
https://cloud.google.com/solutions/mirroring-gitlab-repositories-to-cloud-source-repositories

Go to the Cloud Build setting tab and enable the Kubernetes Engine service and add the following role Deployment Manager Editor (deploymentmanager.deployments.create) to the service account:

```
gcloud projects add-iam-policy-binding devops-lvl1 \
--member=serviceAccount:726322881609@cloudbuild.gserviceaccount.com \
--role=roles/deploymentmanager.editor```

Deployment Manager Templates provided by: https://cloud.google.com/foundation-toolkit