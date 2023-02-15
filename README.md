# pihole-unbound

# Change only .env
# Start
docker-compose pull

docker-compose up -d

# Update
docker-compose down

docker-compose pull

docker-compose up -d --force-recreate
