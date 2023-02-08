https://papermc.io/downloads#Velocity

1. Download Velocity and place it inside a contained folder

2. Create a start.bat or start.sh | diffrent for [Linux](https://docs.papermc.io/velocity/getting-started)

start.bat Windows
``` java
@echo off  
java -Xms512M -Xmx512M -XX:+UseG1GC -XX:G1HeapRegionSize=4M -XX:+UnlockExperimentalVMOptions -XX:+ParallelRefProcEnabled -XX:+AlwaysPreTouch -jar velocity.jar  
pause
```

### Configuring `velocity.toml`

1. Change bind if needed | port number most important

See [[Velocity#Server Config|Server Config]]

2. Change \[Server\] **port** to the desired server, ip if server is of premise

```
lobby = "127.0.0.1:25565"
```

3. player-info-forwarding-mode = | bungeeguard for 1.8.8+ | Modern = 1.13+ | 

```
player-info-forwarding-mode = "bungeeguard"
```

bungeeguard requires extra config and the [BungeeGuard](https://www.spigotmc.org/resources/bungeeguard.79601/) Plugin


# Server Config

### `server.properties`

Enables proxy to connect to the server
```
online-mode=false
```

Here you can change the server port
```
server-port=25565
```

### Forwarding secret

1. Note down the **forwarding.secret** in the velocity proxy folder 

`forwarding.secret` File | Make a random secret longer or shorter:

``` secret
JRxe2kZ2d4ipie4tgmG5Hni6CKlXMSSkXpVa3EYgSSeTleuVgLVorjmEm2WnUj7KZ5MAlsvGelJ
```


### Modern ( More Secure ) [[Velocity#BungeeGuard ( Supports older versions )|Skip to BunggeGuard ->]]

based on `player-info-forwarding-mode: modern`
Minecraft 1.13+ 

**ON SERVER**

##### `config/paper-global.yml`

``` yml
velocity:
	enabled: true
	online-mode: true
	secret: 'JRxe2kZ2d4ipie4tgmG5Hni6CKlXMSSkXpVa3EYgSSeTleuVgLVorjmEm2WnUj7KZ5MAlsvGelJ'
```

secret = [[Velocity#Forwarding secret|Forwarding Secret]] 
online mode = matching online-mode in `velocity.toml` | most likely true

> **Config Done** Add more servers if needed [Docs](https://docs.papermc.io/velocity/player-information-forwarding)


### BungeeGuard ( Supports older versions )

based on `player-info-forwarding: bungeeguard`
Minecraft 1.8+ | if older versions (1.7.2 ) are needed see [Docs](https://docs.papermc.io/velocity/player-information-forwarding#configuring-legacy-bungeecord-compatible-forwarding)

**ON SERVER**

##### `spigot.yml`

``` yml
settings:
  bungeecord: true
```

___

Download [BungeeGuard](https://www.spigotmc.org/resources/bungeeguard.79601/) Plugin.jar and put it in the `server/plugins` folder
**Restart server**

##### `plugins/BungeeGuard/config.yml`

``` yml
allowed-tokens:
  - "JRxe2kZ2d4ipie4tgmG5Hni6CKlXMSSkXpVa3EYgSSeTleuVgLVorjmEm2WnUj7KZ5MAlsvGelJ"
```

**Restart server**

[BungeeGuard install DOCS](https://github.com/lucko/BungeeGuard/blob/master/INSTALLATION.md)

> **Config DONE** [Docs](https://docs.papermc.io/velocity/player-information-forwarding)


___
___

For support with older clients / servers see [[OLD Servers + Clients]]

