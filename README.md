# Deploying MongoDB using K8s (Kubernetes)
In the current repository you can find containers orchestrated configuration with K8s so MongoDB could be run locally by using Minikube.
# Pre-requisites
1. Installed Minikube
2. Kubectl
3. Pulled docker images (mongo and mongo-express). [NOTE: it will save time than pulling along with K8s running]
# Installation
1. To ease the routine of work, there was usage of YAML which lets set necessary parameters inside of the file than using "kubectl create deployment". Since direct command on CLI of K8s is time-consuming.
2. For the "Deployment" there were used mongo and mongo-express. For their communication was used "Service".
3. In order to set up an authorization was used "keys" such as "db-username" and "db-password". [NOTE: when keys are being alternated, need to encode them based on base64]
4. For the file demonstration was created a simple "ConfigMap" file.
5. When all files are ready, the next step is running "kubectl apply -f db-demo.yaml" "kubectl apply -f db-keys.yaml" "kubectl apply -f mongodb.yaml"
![Screenshot from 2024-03-26 13-00-34](https://github.com/BiggieBroo/K8s_MongoDB/assets/140602458/91f1d3f6-204c-4da6-a174-f8ce31b59064)
6. As soon as all of the files are deployed, then we can use "minikube service mongo-express" to see MongoDB GUI.
![Screenshot from 2024-03-26 13-08-41](https://github.com/BiggieBroo/K8s_MongoDB/assets/140602458/3677b5bd-ef6a-4c62-88a9-76f47c2b038a)
![Screenshot from 2024-03-26 13-12-48](https://github.com/BiggieBroo/K8s_MongoDB/assets/140602458/a7303da8-ce73-4f09-a41d-9c1aea7b4804)

