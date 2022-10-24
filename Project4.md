## Implementation of a simple Book Register web form using MEAN stack

### Step 1: MEAN Stack Deployment to Ubuntu in AWS
- Install NodeJs
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
![2 - NodeJS installation](https://user-images.githubusercontent.com/114569323/197567123-22af8b4e-6bbe-4307-a3c0-b431dc78d32c.png)
- Install MongoDB
  - Database Field preparation
    - sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6
    - echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list
![3 - MongoDB installation](https://user-images.githubusercontent.com/114569323/197571315-4f2dbead-dd53-4b3c-8b6e-b718a7f864d7.png)
  - Install MongoDB
    - sudo apt install -y mongodb
    - sudo service mongodb start
    - sudo systemctl status mongodb
![4 - starting the MongoDB service and checking the status](https://user-images.githubusercontent.com/114569323/197571323-529ca85e-c2cb-41f6-a8eb-61aa98f05dbb.png)
  - Install npm – Node package manager
    - sudo apt install -y npm
    - sudo npm install body-parser
    - mkdir Books && cd Books
  - Initialize npm
    - npm init
  - Add a file to it named server.js
     - vi server.js

  ![5 - server code in the server js file](https://user-images.githubusercontent.com/114569323/197573538-7cc017ee-479f-46e3-8f67-e172f3d8fbcc.png)
### Step 2: Install Express and set up routes to the server
- Install Express and set up routes to the server
  - Install Mangoose package, create a file and add the code on the server
    - sudo npm install express mongoose
    - mkdir apps && cd apps
    - vi routes.js
    - mkdir models && cd models
    - vi book.js
    
![6 - installation of the ExpressJS WAF](https://user-images.githubusercontent.com/114569323/197577880-80de6b3c-c1bd-421e-94b8-470e8a3b0a7c.png)
- Access the routes with AngularJS (navigate back to the Books directory)
      - mkdir public && cd public
      - vi script.js
      - vi index.html
  - Start the NodeJS server
    - node server.js
  - Accessing the Book Register web application from the Internet using Public IP address
![7 - accessing my Book Register web application from the Internet using Public IP address](https://user-images.githubusercontent.com/114569323/197578449-0383afef-3b60-4a68-9cce-7605d8ff5360.png)


