# DevOps-Tools
mkdir -p data extensions logs postgres
sudo chown -R 1000:1000 data extensions logs postgres
sudo chmod -R 775 data extensions logs postgres
docker compose up -d
docker logs -f sonarqube
SonarQube is operational
