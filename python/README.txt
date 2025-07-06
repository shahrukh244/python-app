
docker build -f Dockerfile -t glb:5000/python-app:V1 .
docker push glb:5000/python-app:V1


# kubectl apply -f  1-namespace.yaml
# kubectl get ns | grep -i python-app


# kubectl apply -f 2-mysql-pv.yaml
# kubectl get pv -n python-app | grep -i mysql-pv


# kubectl apply -f 3-mysql-pvc.yaml
# kubectl get pvc -n python-app | grep -i mysql-pv
# kubectl get pv -n python-app | grep -i mysql-pv


# kubectl apply -f 4-mysql-secret.yaml
# kubectl get secret -n python-app


# kubectl apply -f 5-mysql-configmap.yaml
# kubectl get cm -n python-app


# kubectl apply -f 6-mysql-deployment.yaml
# kubectl get po -n python-app | grep -i MySQL


# kubectl apply -f 7-mysql-service.yaml
# kubectl get svc -n python-app


# kubectl apply -f 8-phpmyadmin-configmap.yaml
# kubectl get cm -n python-app | grep -i phpMyAdmin


# kubectl apply -f 9-phpmyadmin-deployment.yaml
# kubectl get po -n python-app | grep -i phpMyAdmin


# kubectl apply -f 10-phpmyadmin-service.yaml
# kubectl get svc -n python-app | grep -i phpMyAdmin


# kubectl apply -f 11-phpmyadmin-ingress.yaml
# kubectl get ing -n python-app


# kubectl apply -f 12-flask-secret.yaml
# kubectl get secret -n python-app | grep -i flask


# kubectl apply -f 13-flask-deployment.yaml
# kubectl get po -n python-app | grep -i flask


# kubectl apply -f 14-flask-service.yaml
# kubectl get svc -n python-app | grep -i flask


# kubectl apply -f 15-flask-ingress.yaml
# kubectl get ing -n python-app | grep -i flask

