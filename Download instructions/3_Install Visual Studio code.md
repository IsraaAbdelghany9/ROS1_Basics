# Installing Visual Studio Code on Ubuntu

Visual Studio Code is a popular code editor that provides many features for development. Follow the steps below to install it on Ubuntu.

## Visual Studio Code Installation on Ubuntu:


## 1-Update Your Package List
```sudo apt update -y```

## 2-Install Required Packages
```sudo apt install -y software-properties-common apt-transport-https wget```

## 3-Import the Microsoft GPG Key
```wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -```

## 4-Add the Visual Studio Code Repository
```sudo add-apt-repository -y "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"```


## 5-Update Your Package List Again
```sudo apt update -y```

## 6-Install Visual Studio Code
```sudo apt install -y code```
