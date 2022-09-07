# Linux (Ubuntu 20.04)

```make
sudo apt-get install gnupg
wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -

echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list

sudo apt-get update

sudo apt-get install -y mongodb-org

ps --no-headers -o comm 1 // 초기화

sudo systemctl start mongod
sudo systemctl daemon-reload

sudo systemctl status mongod

sudo systemctl stop mongod

sudo systemctl restart mongod

mongosh
```

# Mac

하단 링크 참고  
https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/  

# Windows

https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-windows/  
