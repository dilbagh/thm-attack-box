# TryHackMe Attack Box

This project makes use of Kali linux image and sets it up with OpenVPN connection with TryHackMe.

## How to setup

* Clone this repo.

* Login to your TryHackMe account.

* Visit https://tryhackme.com/manage-account/access-open-vpn

* Choose a server closest to you. Example: `IN-Regular-1` if you are in India.

* Download the configuration file. Put it in the `config` folder of this repo. Name it `vpn-config.ovpn`.


## How to run

* Open a terminal in the project folder.

* Run:
```bash
> sudo docker compose up -d
```
Note: It's necessary to use sudo in order to use some VPN and some other networking tools inside the docker container.

This will start the container and connect it to your VPN profile.

* Connect to the container by running:
```bash
> docker exec -it thm-attack-box-thm-attack-box-1 /bin/bash
```

* To stop the container, run:
```bash
> sudo docker compose down
```