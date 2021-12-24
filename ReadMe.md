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

docker push localhost:32000/csharpauth:1.6
microk8s helm3 install csharpauth ./csharpauth
