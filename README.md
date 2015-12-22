# notifications-history
The service for managing users' notification plans

#Build
docker build -t wkicior/notification-plans .

# Run
docker run --privileged=true -it -v [absolute path to project directory]:/app:rw --rm -p 9999:9000 --link notification-plans-mongo:notification-plans-mongo wkicior/notification-plans

#Usage
curl -v -X POST http://localhost:9999/notifications -H "Content-Type: application/json" -d "{ \"name\" : \"wojtek\", \"favoriteNumber\" : 12 }"

