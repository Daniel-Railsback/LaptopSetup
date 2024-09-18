List of apps to install
```
git
Docker
Go
vscode
Neovim
tmux
```


# Install commands: 

*Git*
[Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
[Email & Username doc](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git?platform=linux)

```
# Install Git
sudo apt install git-all
# Set git User.Name
git config --global user.name "Daniel-Railsback"

# Test git User.Name
git config --global user.name

# Set git email
git config --global user.email "Daniel.railsback@improvementpath.com"

# Test git email 
git config --global user.email
```

*Docker*
[Doc](https://docs.docker.com/engine/install/ubuntu/)
```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# Install Latest version of Docker package
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Test 
sudo docker run hello-world
```

*GoLang*
[Install doc](https://go.dev/doc/install)

```
# Download GoLang package | Move to install dir
sudo wget /usr/local wget https://go.dev/dl/go1.23.1.linux-amd64.tar.gz

# Remove any old versions & grab the lastest version of GoLang
# If Go folder exist you MUST run the rm -rf & let the application create the Go folder
# If this is a new install of go: Start at "sudo tar - C"
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.23.1.linux-amd64.tar.gz

# Add Go to PATH
export PATH=$PATH:/usr/local/go/bin



#Verify verson:
go version


```

*neovim*
```
#Install neovim
sudo apt install neovim
```

*Vscode*
[Install Doc](https://code.visualstudio.com/docs/setup/linux)
```

cd /usr/local
# Download needed .deb file: 
wget -O  /usr/local/code.deb https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64

#install code
sudo apt install /usr/local/code.deb
# if not prompted
# echo "code code/add-microsoft-repo boolean true" | sudo debconf-set-selections

# Install apt registries
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" |sudo tee /etc/apt/sources.list.d/vscode.list > /dev/null
rm -f packages.microsoft.gpg

#Finalize install
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders


# Launch vscode
code .



```

*tmux*
```
# Install tmux
sudo apt install tmux
```


## Next up
[Docker env setup on Tree House]()

