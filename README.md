# CS2 on Pterodactyl

Docker image and Pterodactyl egg to prepare for upcoming CS (CS:GO/CS2) updates. The Docker image is based on the Valve provided SteamRT3 Sniper package, with the Pterodactyl egg featuring a few exposed variables such as Beta selection variables and allowing for skipping SteamCMD on launch (i.e, preventing updates). This should allow existing CSGO servers to easily stay on the opt-in CS:GO branch once CS2 releases.

This setup is very similar to the stock Pterodactyl Source server setup, so things should be familiar once imported.

The underlying Docker image is based on Valve's Steam Runtime 3 (Sniper), which should be able to run both CS:GO and CS2 without any issues. The image also can be rebuilt easily as soon as Valve updates their base SteamRT3 image, so we can stay on top of their updates without worrying too much about it. 

## How to use

- Download egg(s) from the `/pterodactyl` directory.
  - `cs2.json`: Egg for CS2
  - `csgo.json`: Egg for CS:GO
- Import into your Pterodactyl nest of choice. [Read here if you need a guide on how to do this.](https://github.com/parkervcp/eggs#how-to-import-an-egg)

## I want to use the SteamRT3 Docker image directly

The Docker image is hosted on the GitHub Container Registry. You can grab it from here: 
```
ghcr.io/1zc/steamrt3-pterodactyl:latest
```

Alternatively, you can find a full list of builds here: https://github.com/1zc/CS2-Pterodactyl/packages
