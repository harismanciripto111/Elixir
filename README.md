# Elixir
new elixir run
#AWALAN, GAUSA BANYAK TANYA PASTE PASTE AJA KALO ERROR BARU NANYA

'''bash
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

'''bash
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg


'''bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


'''bash
sudo apt-get update


'''bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


'''bash
wget https://files.elixir.finance/Dockerfile


'''bash
nano Dockerfile
namain nanti di moniker dc sendiri


'''bash
docker build . -f Dockerfile -t elixir-validator

'''bash 
docker run -d --restart unless-stopped --name ev elixir-validator
