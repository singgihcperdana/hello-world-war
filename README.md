# hello-world-f8
Deploy aplikasi hello-word ke openshift dengan maven plugin fabric8

## 1. Terlebih dahulu buat ConfigMap berikut untuk mengisi properti greeting.message
```aidl
apiVersion: v1
kind: ConfigMap
metadata:
  name: hello-world-f8-config-map
  namespace: spring-app
data:
  greeting.message: Hello World aja deh!!!
```

## 2. Untuk deploy ke openshift
```aidl
mvn fabric8:deploy
```