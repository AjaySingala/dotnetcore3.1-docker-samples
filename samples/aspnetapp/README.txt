#Ref url: https://github.com/dotnet/dotnet-docker/tree/master/samples/aspnetapp

#Directly run sample:
#docker run --name aspnetcore_sample --rm -it -p 8000:80 mcr.microsoft.com/dotnet/core/samples:aspnetapp

#Build the image.
docker build --pull -t aspnetapp .

#Run the container.
docker run --name aspnetcore_sample --rm -it -p 8000:80 aspnetapp

#Build and run locally.
dotnet run

#After the application starts, visit http://localhost:5000 in your web browser.

#You can produce an application that is ready to deploy to production locally using the following command.

dotnet publish -c Release -o out
#You can run the application using the following commands.

cd out
dotnet aspnetapp.dll
