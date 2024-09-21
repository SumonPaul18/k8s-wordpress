## Deploy WordPress On Kubernetes

#### Copy & Paste & Enter
~~~
rm -rf k8s-wordpress
git clone https://github.com/SumonPaul18/k8s-wordpress.git
kubectl apply -f k8s-wordpress/wp-deploy/wordpress-namespace.yaml
kubectl apply -f k8s-wordpress/wp-deploy/.
kubectl get pod,deploy,svc,pvc,pv,ns -n wp
~~~