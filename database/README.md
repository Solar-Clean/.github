# Install MongoDB

With only one command:

```
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add - && echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list && sudo apt update && sudo apt install -y mongodb-org
```

# Start the database

Start the MongoDB service with:

```
sudo systemctl start mongod.service
```

You can check if everything is well set up and running with: 

```
sudo systemctl status mongod
```

To allow MongoDB to start automatically on system boot you can run:

```
sudo systemctl enable mongod
```

# Issue handling

Sometimes the MongoDB service demon crashes and the database is no longer available. To restart the database run:

```
sudo systemctl restart mongod
```

To stop the database service:

```
sudo systemctl stop mongod
```

And to start it again do:

```
sudo systemctl start mongod
```

> Remember that you can always check if your database is up and running with calling _systemctl_ with `status mongod`

# UI for the database

Additionally to view your entries you can download the MongoDB compass here: https://www.mongodb.com/try/download/compass
