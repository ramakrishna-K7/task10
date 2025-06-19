                                 Implemented GitOps pipeline using ArgoCD and Kubernetes ________________________________________
STEP 1: Launch EC2 Instance
Master:
•	AMI: Amazon Linux Kernel 5.10
•	Instance Type: t2.medium
•	EBS Volume: 28GB
Nodes: 2-instances
•	AMI: Amazon Linux Kernel 5.10
•	Instance Type: t2.micro
•	EBS Volume: 28G
________________________________________
STEP 2:  Install docker, Kubernetes and argocd
•	I have downloaded argocd with help of helm
________________________________________
STEP 3: Git repo with manifest files
Files: 
•	Deployment.yml
•	Service.yml
________________________________________
ArgoCD screenshots showing sync in action:

 ![image](https://github.com/user-attachments/assets/b9311512-c2f0-46b4-8f0c-40620de6ca5f)

________________________________________
Video/notes explaining GitOps flow:

Log in to ArgoCD UI
Access the ArgoCD web interface 
Create a New Application
  •	On the left sidebar, click "New App".
Fill in Application Details
  •	Application Name: A unique name for your app
  •	Project: Leave as default unless you've created a custom project.
  •	Sync Policy:
    o	Choose Manual 
    o	Automatic 
 Specify the Git Repository
  •	Repository URL: Paste your GitHub repo link 
  •	Revision: Select the branch 
  •	Path: Directory containing your Kubernetes manifests 
 Set the Deployment Destination
  •	Cluster URL: https://kubernetes.default.svc 
  •	Namespace: Choose where to deploy your app 
 Save and Deploy
  •	Click "Create"
  •	Your app will now appear in the dashboard
  •	If using Manual sync, click "Sync" to deploy
  •	If using Auto-sync, ArgoCD will deploy it automatically when it detects changes








