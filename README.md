# Gloo Edge via GitOps
This repo holds source manifests and ArgoCD Application manifests for demoing configuring Gloo Edge via ArgoCD.

Prerequisites:
- You must have installed Gloo Edge into your cluster. Instructions for doing so via `glooctl` can be found in this blog post: https://www.solo.io/blog/from-zero-to-gloo-edge-in-15-minutes/. In order to test the various versions of httpbin, you will need to expose the Gloo Edge Gateway in your cluster. Instructions for doing so if you are running a cluster via KinD can be found in that same blog post.
- You must have installed ArgoCD into your cluster. Instructions for doing so can be found in this wiki page under step #1: https://argo-cd.readthedocs.io/en/stable/getting_started/. If you want to get a visual of the ArgoCD applications, you will need to expose the ArgoCD UI endpoint and retrieve the admin password from the secret in the `argocd` namespace. Instructions for doing so are in the same blog post

Note: It is not recommended to install any of these Applications side by side, as they are not configured to run in the same namespace at the same time. You will likely encounter issues with colliding manifests, conflicting Virtual Service domains, etc if you attempt it.
