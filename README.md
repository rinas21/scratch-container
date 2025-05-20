### Build the contaienr
podman build -t app-scratch-container .

### Map host machine port 6000 to app running in the container on port 5000

podman run -d -p 6000:5000 app-scratch-container

### Check the status of the running app
podman ps

### Access the application in the container from the host node.
curl http://localhost:6000

### Stop the app running in the contaienr 
podman stop 00245880310a
