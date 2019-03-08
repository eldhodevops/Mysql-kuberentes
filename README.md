# mysql-kuberentes
Mysql deployment for kubernetes

#Build Image
```
Build dockerimage from the provided dockerfile and provide the name in the deploy.yml file 
```
# Timezone setting

You can give custom time zone as env variable

```
 - name: TIMEZONE
   value: 'Asia/Kolkata'
            
```
create database credentials  using secrets in k8's

```
kubectl create secret generic mysql-credentials --from-literal=rootpw=rootpass --from-literal=dbname=test --from-literal=dbuser=testuser --from-literal=dbpasswd=rootpasworddd
```
