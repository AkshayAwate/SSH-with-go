# SSH-with-go
SSH into nginx container with username and password.

# Run nginx container
```sh
docker run -d --name nginx nginx 
docker exec -it nginx bash
apt-get update
apt-get install openssh-server
service ssh start
```

# Add new user 
```sh
adduser akshay
```

# Modify /etc/ssh/sshd_config to add user akshay
```sh
AllowUsers akshay
```

# SSH with below command

```sh
ssh akshay@ip-of-container
```

Change the IP address of container and username, password in main.go and run ```go run main.go```, this will ssh into container and prints login name.