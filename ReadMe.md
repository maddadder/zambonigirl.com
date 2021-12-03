# Dependencies

dotnet add package Microsoft.Identity.Web
dotnet add package Microsoft.AspNetCore.Authentication.OpenIdConnect
dotnet add package Microsoft.Identity.Web.UI

# Docker
docker-compose build

# Testing
docker-compose up

# Deploy to microk8s
docker push localhost:32000/csharpauth:1.0

microk8s kubectl apply -f microk8s.yaml
