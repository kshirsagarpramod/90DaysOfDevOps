# Prerequisites:-

Update the packges to the latest:- 
        
    sudo apt-get update

Install Docker: 

    sudo apt-get install docker.io

Add current user to the docker group: 

    sudo usermod -aG docker $USER

Use the new docker group: 

    newgrp docker      

Check Docker is installed:

        docker ps

## Install Kind

    curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64

Make it executable

    chmod +x ./kind

Move it to a directory in your PATH

    sudo mv ./kind /usr/local/bin/kind

To check installed kind version

    kind --version
OR

    kind version    


## Install kubectl

    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

Make it executable

    chmod +x kubectl

Move it to a directory in your PATH

    sudo mv ./kubectl /usr/local/bin/kubectl

To check installed kubectl version

    kubectl version
