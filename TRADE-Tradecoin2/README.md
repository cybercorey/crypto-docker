# Getting Started
```sh
# Clone this Repo
git clone https://github.com/cybercorey/crypto-docker
# Select Tradecoin
cd crypto-docker/TRADE-Tradecoin2
# Generate VNC password (only needed once)
x11vnc -usepw
# Build docker image (go grab a beer and wait :)!)
docker build -t crypto-docker-trade . 
# Shared data dir, you may also want to create tradecoin.conf and add a few nodes
mkdir /home/$USER/.tradecoin
# Run the docker!
docker run -d -it --rm -p 5900 --mount type=bind,source=/home/$USER/.vnc,destination=/root/.vnc --mount type=bind,source=/home/$USER/.tradecoin,destination=/root/.tradecoin crypto-docker-trade
```


Next...
```sh
docker ps
```
This will give you a display of all your running containers.  Hopefully you'll see **crypt-docker-tradecoin** and can determine which port on the local host it's using.

Finally, run your VNC viewer of choice and connect to that port on localhost.  For example, if you see that port 5900 in the container has been mapped to port 32768 on the host, you would connect to 127.0.0.1:32768.  Recall that you'll need the password you set for x11vnc earlier.

# Tip Jar

trade: TFWpS66gtYzq3bRn3u9bPrkj4UNaoNG6U3
