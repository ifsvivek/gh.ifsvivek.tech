---
title: Set up ChatGPT locally using Ollama and open webui
date: 2024-05-05 00:00:00 -500
categories: [ai, chatgpt, ollama, guide]
tags: [ai, chatgpt, ollama, guide]
---

# Set up ChatGPT Locally Using Ollama and Open Webui

## Introduction

In this guide, we will set up ChatGPT locally using Ollama and open webui.

### Install WSL2 and Ubuntu 20.04
- Use this command to install WSL2 and Ubuntu 20.04
```bash
wsl --install
```

![](https://imgur.com/xZl6AWO.png)

- After installation, open Ubuntu 20.04 and set up your username and password.

![](https://i.imgur.com/DZVCuah.png)

- Update and upgrade the system
```bash
sudo apt update && sudo apt upgrade -y
```


![](https://i.imgur.com/o5YFqw4.png)


![](https://i.imgur.com/25iDmrA.png)


### Install Ollama

- Use this command to install Ollama
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
or visit [Ollama](https://ollama.com/download/linux) and follow the instructions.


![](https://i.imgur.com/HpG0L4O.png)

![](https://i.imgur.com/E3Z9Ooi.png)

![](https://i.imgur.com/rCg2tjt.png)

- After installation, you can check that Ollama is installed by opening browser and visiting [http://localhost:11434/](http://localhost:11434/)


![](https://i.imgur.com/mgoUNTx.png)


- Now download the AI model from [Ollama](https://ollama.com/models)
- Then run the following command to install the model
```bash
ollama install <model-name>
```

![](https://i.imgur.com/lChaqAA.png)

![](https://i.imgur.com/ftADIIm.png)

![](https://i.imgur.com/YAVrLsw.png)

- Now your AI model is installed and running. You can stop the model by running the following command
```bash
/bye
```

### Installing Docker

- Use this command to install Docker

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```


![](https://i.imgur.com/tHy5f6K.png)

- Install Docker
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```


![](https://i.imgur.com/XbbhGuW.png)

- or visit [Docker](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository) and follow the instructions.

### Install Open Webui

- Use this command to install Open Webui
```bash
sudo docker run -d --network=host -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

![](https://i.imgur.com/2CDXp8L.png)

- Now you can check that Open Webui is installed by opening browser and visiting 
  - [http://localhost:3000/](http://localhost:3000/)
  - [http://localhost:8080/](http://localhost:8080/)

- Create a new user and login to Open Webui

![](https://i.imgur.com/8bNjMDI.png)


![](https://i.imgur.com/u15tkri.png)

- Now you can click on the settings icon and add the Ollama API URL

![](https://i.imgur.com/CMKYpDJ.png)

![](https://i.imgur.com/1b7T0Wg.png)

- Now you can start chatting with your AI model by selecting the model and clicking on the chat icon


![](https://i.imgur.com/oZre8yg.png)

### Additional Models Installation

- You can click on the settings and click on the models tab
- Then enter the model name and click on the install button

![](https://i.imgur.com/8TrkZQW.png)

![](https://i.imgur.com/yRXcoPA.png)

- You can change the model by clicking on the top left corner and selecting the model

![](https://i.imgur.com/REzHWmJ.png)


### More Information
- To stop the Open Webui container, use this command
```bash
sudo docker stop open-webui
```

- To start the Open Webui container, use this command
```bash
sudo docker start open-webui
```

- To remove the Open Webui container, use this command
```bash
sudo docker rm open-webui
```

- To stop wsl2, use this command
```bash
wsl --shutdown
```

- To uninstall Unbuntu, use this command
```bash
wsl --unregister Ubuntu
```
- To uninstall WSL2, use this command
```bash
wsl --uninstall
```


## My Links
- [GitHub](https://github.com/ifsvivek)
- [Twitter](https://twitter.com/ifsvivek)
- [LinkedIn](https://www.linkedin.com/in/ifsvivek/)