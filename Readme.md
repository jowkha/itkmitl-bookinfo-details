# How to run details service

## Prerequisite

* Ruby 2.7

```bash
ruby details.rb 9080
```

## How to run with Docker

```bash
# Build Docker Image for details service
docker build -t details .

# Run details service on port 8081
docker run -d --name details -p 8081:8081 details
```

* Test with path `/details/1` and `/health`


## How to run with Docker Compose

```bash
docker-compose up
```
## Build amd Push Docker Image
```bash
# Build Ratings Service Docker Image
docker-compose build

export TOKEN=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
export GITHUB_USER=jowkha
echo $TOKEN | docker login ghcr.io --password-stdin --username $GITHUB_USER
docker push ghcr.io/jowkha/bookinfo-details:dev
```

## How to run kubectl

```bash
# Create deployment resource
kubectl apply -f k8s/

# Check status of each resource
kubectl get deploy,pod,svc,ingress
```
## How to check 

```bash
curl http://itkmitl.bookinfo.dev.opsta.net/student3/details/health
```