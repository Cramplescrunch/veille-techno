# Documentation sur l'isntallation et l'utilisation de MongoDB

## Installation

Pour l'installation, tout est expliqué sur le site de MongoDB à l'adresse suivante : https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/

## Documentation

### Run MongoDB as a service

Quote from [this StackOverflow answer](https://stackoverflow.com/questions/52068925/what-does-it-mean-to-install-mongodb-as-a-service) : 

> What are services?

Services are application types that run in the system's background. These are applications such as task schedulers and event loggers. If you look at the Task Manager > Processes, you can see that you have a series of Service Hosts which are containers hosting your Windows Services.

What difference does setting MongoDB as a service make?

Running MongoDB as a service gives you some flexibility with how you can run and deploy MongoDB. For example, you can have MongoDB run at startup and restart on failures. If you don't set MongoDB up as a service, you will have to run the MongoDB server every time.

So, what is the difference between a network service and a local service?

Running MongoDB as a network service means that your service will have permission to access the network with the same credentials as the computer you are using. Running MongoDB locally will run the service without network connectivity.(Refer Source here)


