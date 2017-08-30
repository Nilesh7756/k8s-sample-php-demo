wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/sample-namespace.yaml

wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/demo-sample-php.yaml

wget https://raw.githubusercontent.com/Nilesh7756/k8s-sample-php-demo/master/demo-sample-php-svc.yaml

kubectl -n demo-namespace

kubectl -f sample-namespace.yaml

kubectl get ns

kubectl get deployment -n demo-namespace

kubectl create -f demo-sample-php-svc.yaml

kubectl get svc -n demo-namespace

kubectl delete -f demo-sample-php-svc.yaml

kubectl delete -f demo-sample-php.yaml

kubectl delete -f sample-namespace.yaml
