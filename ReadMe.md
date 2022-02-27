# Dependencies

dotnet add package Microsoft.Identity.Web
dotnet add package Microsoft.AspNetCore.Authentication.OpenIdConnect
dotnet add package Microsoft.Identity.Web.UI

# Docker
docker-compose build

# Testing
docker-compose up

Navigate to http://localhost:5001

# Done Testing?
docker-compose down

# Deploy to microk8s

docker push 192.168.1.151:32000/zambonigirl:1.0.11
microk8s helm3 install zambonigirl ./zambonigirl

# daffy
helm install zambonigirl ./zambonigirl --namespace websites
