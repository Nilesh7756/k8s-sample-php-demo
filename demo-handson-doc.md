wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/sample-namespace.yaml

wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/demo-sample-php.yaml

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
