# Silence

Silence - a P2P, E2E encrypted private messaging service

Regaining your silence
  

## Setting Up a Server
### Initial Setup

```console

# clone repo

$ git clone https://github.com/projectsilence/silence-server

  

# cd into directory

$ cd silence-server

  

# start mysql service

$ apt-get install mysql # if not already installed

$ sudo service mysql start

  

# edit configuration of setup.go

$ nano setup.go

# CHANGE THIS to your desired database

  

const (

username = "root" # Local user to make database

password = "rootpassword" # Password for local user

hostname = "127.0.0.1:3306" # Host for database to be created

dbname = "silenceserver" # Name you want for the database

)

  

# run the script

$ go run setup.go

```

### Running the server (server.go still a work in progress)

```console

# ( Optional ) Build the server - not recommended due to "allowed IPs"

$ go build server.go

# Run the serevr

$ go run server.go

```

## WARNING - Only run a server on a secure server/machine