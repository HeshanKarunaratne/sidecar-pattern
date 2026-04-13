# How to deploy to K8s

1. Create docker images for both services inside respective folder

```cmd
docker build -t book-service:1.0 .
docker build -t log-service:1.0 .
```

2. Create the deployment and service respectively

```cmd
kubectl apply -f k8s-deployment.yaml
kubectl apply -f k8s-service.yaml
```

3. Forward port to the service to work in web browser

```cmd
kubectl port-forward service/combined-service 8080:80
```

4. Use below curl to add a book

```cmd
curl --location 'http://localhost:8080/api/books' \
--header 'Content-Type: application/json' \
--data '{
    "id": "1",
    "title": "Death Note",
    "author": "Japan Sensei"
}'
```

4. Use below curl to get books

```cmd
curl --location 'http://localhost:8080/api/books'
```