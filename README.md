# My_first_app_on_GKE_K8s
My first app developed on GCP App Eng; Cloud Run and GKE
[Disclaimer:  ***Do not use the contents of this repository in your production.***]
Static website on Google Cloud Platform K8s:  bandkarma.org
This repository details my first containerized application on GKE [Google Kubernetes Engine] Kubernetes [K8s] cluster.  The application is a very simple file server written in GO and deployed in a standard GKE K8s cluster of e2-micro 15GB in Google Cloud Platform US-West-1; -4.  The application is a static website that serves files from a GCP cloud storage bucket in UW-West.  The GKE K8s is a high octane platform for such a static application.  I am using this GCP project as a k8s - cloud  learning platform.   

I used Google AppEngine to containerize my application image from my GCP cloud console storage.   This created a [vm] in US-West for the garage band website:  bandkama.org.  The next step was to use GCP Cloud Run to create an on-demand containerized application. The build was easy using the cloud run console on gcp - no cloud editor or additional docker files needed.  The app engine image had a micro-docker symbol next to it.  This step used an image in gck.io.   I am using a reserved IP address and Google managed SSL certification into a node port of the GKE cluster.  

I focused on the cost of K8s operations to save money.  AppEngine cost $92 for one month.  The first month deployment was in an auto cluster of E2 e2-mediums at $158/month.  I deleted this cluster and re-deployed in a standard GKE cluster of e2-micro linked to dual zone storage bucket: $46/month per after discounts.  The ultimate cost savings would be to use on-demand Cloud Run.    

My future projects will be to create a service mesh for the cluster.  The YAML files in this repository have been edited to remove critical identification factors of GCP.

