# ASPNetCoreMessenger
Steps to run:

1) 
```
docker network create --driver nat --subnet=172.18.0.0/16 myNetwork
```

2) 
```
cd MessengerAPI/
docker-compose build
docker run --network myNetwork --ip 172.18.0.22 --name messengerAPIContainer messengerapi
```

3) 
```
cd MessengerUI/
docker-compose build
docker run --name messengerUIContainer messengerui
```

4) 
```
docker exec messengerUIContainer ipconfig
```

5) 
```
go to IP of UI Container in your browser
```