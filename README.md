Qdrant Installation steps in linux : 

sudo apt update
sudo apt install docker.io -y
sudo systemctl enable docker
sudo systemctl start docker
docker --version
sudo usermod -aG docker $USER
newgrp docker
 docker ps
groups
 docker pull qdrant/qdrant
mkdir -p ~/qdrant_data
"docker run -d \
   --name qdrant \
   -p 6333:6333 \
   -p 6334:6334 \
   -v ~/qdrant_data:/qdrant/storage \
   qdrant/qdrant"
docker ps
http://localhost:6333/dashboard
