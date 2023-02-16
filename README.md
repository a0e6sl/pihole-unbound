# pihole-unbound

# Change only .env
# Start
docker-compose pull

docker-compose up -d

# Update
docker-compose down

docker-compose pull

docker-compose up -d --force-recreate
# Update root.hints only if its needed
wget https://www.internic.net/domain/named.root -qO- | sudo tee $PWD/unbound/root.hints
