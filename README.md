## Deploy WordPress On Kubernetes

#### Copy & Paste & Enter
~~~
rm -rf k8s-wordpress
git clone https://github.com/SumonPaul18/k8s-wordpress.git
kubectl apply -f k8s-wordpress/wp-deploy/wordpress-namespace.yaml
kubectl apply -f k8s-wordpress/wp-deploy/.
kubectl get pod,deploy,svc,pvc,pv,ns -n wp
~~~
#### How to Browseing The WordPress Site

#### http://Your-k8sClaster-IP:31000

<details>
 <summary> <b> How to Show WordPress Exposed Port: </summary> </b>

Verifying the WordPress Services
~~~
kubectl get svc wordpress -n wp
~~~
We can see like this:
> wordpress   NodePort   10.101.227.25    <none>        80:31000/TCP     11m

So from this verifying Our services are Exposed on Port:31000
</details>

#### Delete the WordPress Deploy
Just Delete WP-MYSQL Deployment
~~~
kubectl delete deploy wordpress,mysql -n wp
~~~

#### Delete the WordPress Deploy All
~~~
kubectl delete ns wp
~~~
#
