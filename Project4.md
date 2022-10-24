## Implementation of a simple Book Register web form using MEAN stack

### Step 1: MEAN Stack Deployment to Ubuntu in AWS
- Installed NodeJs
  - Update Ubuntu server
    - sudo apt update
  - upgrade ubuntu
    - sudo apt upgrade
  - Add certificates
    - sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates
    - curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
![1 - adding certificates after updating and upgrading the ubuntu server](https://user-images.githubusercontent.com/114569323/197560098-96c1e361-225c-4f59-a3e2-e927221479a5.png)

  - NodeJS installation
    - sudo apt install -y nodejs
