#For Creation of Kubernetes cluster please follow below link of medium blog.

https://medium.com/google-cloud/how-to-create-google-container-engine-gke-using-the-google-cloud-platform-console-925dd1cc9400

#Note Do not execute "kubectl proxy" on Active shell (Work station)


#On Active shell create directory demo-kube

mkdir demo-kube

cd demo-kube

#Download sample-namespace file

wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/sample-namespace.yaml

#Download deployment file

wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/demo-sample-php.yaml

#Download kubernetes Service file

wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/demo-sample-php-svc.yaml

#Create "demo-namespace" namespace 

kubectl create -f sample-namespace.yaml

kubectl get namespace

#Create Deployment for sample php App

kubectl create -f demo-sample-php.yaml

kubectl get deployment -n demo-namespace

#Get PODs which were created when deployment kind was created

kubectl get pods -n demo-namespace


#Crerate kubernetes Service

kubectl create -f demo-sample-php-svc.yaml

kubectl get svc -n demo-namespace


#Delete Resources

kubectl delete -f demo-sample-php-svc.yaml

kubectl delete -f demo-sample-php.yaml

kubectl delete -f sample-namespace.yaml
