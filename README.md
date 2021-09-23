## ✌️ || ¿Como instalarlo?

Para instalar el paquete LaMonaLisa necesitas:

- Necesitas instalar [**Node.js**](https://nodejs.org/en/download/).

- Necesitas instalar [**discord.js**](https://npmjs.com/package/discord.js).

Luego puede abrir el terminal de su app y escribir:

```
$ npm install lamonalisa
```

## 🌟 || ¿Que ofrece?

### Funciones:

-  [`BienvenidaImage()`](#BienvenidaImage) - Funcion para crear una imagen de bienvenida.
-  [`Invertir()`](#Invertir) - Invierte el color de una imagen.
-  [`Contraseña()`](#Contraseña) - Genera una contraseña.
-  [`BlurImage()`](#BlurImage) - Genera una imagen borrosa.
-  [`BN()`](#BN) - Genera una imagen en blanco y negro.
-  [`Sepia()`](#Sepia) - Genera una imagen sepia. 
-  [`Blink()`](#Blink) - Genera un gif con dos imagenes.
-  [`Triggered()`](#Triggered) - Genera un gif triggered.
-  [`Links`](#Links) - Links importantes.


# || Funciones:

## BienvenidaImage

- **Modo de Uso**

Si quieres los datos por default deja vacio, por ejemplo tomemos el fondo.
por default sera transparente, y debemos dejarlo de esta menera `.fondo("")`

Fonts disponibles `NC, NG, NGC, Bold, MC, BoldItalic, ExtraBold, ExtraBoldItalic, Italic, Light, LightItalic, Regular, SemiBold, SemiBoldItalic, RL`

```js
const LaMonaLisa = require("lamonalisa");

let wel = new LaMonaLisa.Bienvenida()
  .avatar("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png?size=1024")
  .fondo("https://cdn.discordapp.com/attachments/886073523028754473/888823047832883270/Splash_LaMonaLisa.jpg")
  .titulo("¡Bienvenido WadeSlider#6847!")
  .subtitulo("¡Eres el miembro #30!")
  .font("RL")
  .colortit("#fff")
  .colorsub("#fff")
  .colorcir("#fff")

/*Esto sirve para crear la imagen con los datos proporcionados*/
let img = await LaMonaLisa.BienvenidaImage(wel);

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'Welcome.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "Welcome.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/884935876612849705/890576913528135730/Welcome.gif">

## Invertir

**Modo de uso**

```js
const LaMonaLisa = require("lamonalisa");

/* Aqui creas la imagen con los datos que necesites*/
let img = await LaMonaLisa.invertir("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png");

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'Invertido.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "Invertido.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/886073523028754473/889272043676262420/Invertido.gif">

## Contraseña

**Modo de uso**

```js
const LaMonaLisa = require("lamonalisa");

/* Genera la contraseña */
let contraseña = await LaMonaLisa.Contraseña(16)

message.channel.send("La contraseña es "+contraseña+".")
```

**lo que devuelve**

```
w9mF5OK10D8fQho3
```

## BlurImage

- **Modo de Uso**

```js
const LaMonaLisa = require("lamonalisa");

/*Esto sirve para crear la imagen con los datos proporcionados*/
let img = await LaMonaLisa.BlurImage("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png?size=1024", 5);

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'Blur.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "Blur.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/886073523028754473/889863055687684107/Blur.gif">

## BN

**Modo de uso**

```js
const LaMonaLisa = require("lamonalisa");

/* Aqui creas la imagen con los datos que necesites*/
let img = await LaMonaLisa.BN("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png");

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'BN.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "BN.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/886073523028754473/890589495043436544/BN.gif">

## Sepia

**Modo de uso**

```js
const LaMonaLisa = require("lamonalisa");

/* Aqui creas la imagen con los datos que necesites*/
let img = await LaMonaLisa.Sepia("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png");

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'Sepia.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "Sepia.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/886073523028754473/890593923834200114/Sepia.gif">

## Blink

**Modo de uso**

```js
const LaMonaLisa = require("lamonalisa");

/* Aqui creas la imagen con los datos que necesites*/
let img = await LaMonaLisa.Blink("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png", "https://cdn.discordapp.com/avatars/728259605565800558/c82b9a06041d5184802c9ac495cd8d9a.png");

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'Blink.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "Blink.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/886073523028754473/890598637078450176/Blink.gif">

## Triggered

**Modo de uso**

```js
const LaMonaLisa = require("lamonalisa");

/* Aqui creas la imagen con los datos que necesites*/
let img = await LaMonaLisa.Triggered("https://cdn.discordapp.com/avatars/873940469950849056/5492e536824a2c5c277a0ca3fba80715.png");

/*¿Como mandarla?*/

/*V13 de discord*/

message.channel.send({ 
    files: [{
        attachment: img,
        name: 'Triggered.gif'
    }]
})

/*V12 de discord*/

const { MessageAttachment } = require("discord.js");
let a = new MessageAttachment(img, "Triggered.gif");

message.channel.send(a)
```

**Imagen que devuelve**

<img src="https://cdn.discordapp.com/attachments/886073523028754473/890600800336883782/Triggered.gif">

## Links

<a href="https://discord.gg/6whWRxHVKr">Servidor de soporte</a># lamonalisa

