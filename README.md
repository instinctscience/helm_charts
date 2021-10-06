# Helm Charts used by Instinct Science

This is a collection of Helm charts used by Instinct Science to deploy to EKS. It uses Github pages to publish the repository. So anything commited to `master` is the current repository contents.

## Basic Updating Charts and Releasing
1. Make edits to template files
1. Update Chart.yaml file with new version numbers
1. Create a new tarball `helm package phoenix-app/.`
1. Update Chart index file `helm repo index --url https://instinctscience.github.io/helm_charts/ --merge index.yaml .`
  Note: sometimes this command update the created timestamp of previous releases. These should manually be kept the same and not commited.
1. Commit, PR, merge to `master`