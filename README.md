<p align="center">
    <img src="https://cdn.btch.bz/file/06e8d93a5831ce577b93e.jpg" width="250" alt="logo">
</p>
<h1 align="center">Kιɳα Bσƚ</h1>
<h3 align="center">This bot uses a library from Baileys</h3>
<h3 align="center">Give this repository a ⭐ if you like it</h3>

<div align="center">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![GPL3 License][license-shield]][license-url]

</div>

<div align="center">

[![JOIN WITH OUT COMMUNITY][community-shield]][community-url]

</div>

## Description

<p align="center">
    <img src="https://cdn.btch.bz/file/06e8d93a5831ce577b93e.jpg" width="400" alt="logo">
</p>

-   Kιɳα Bσƚ is a WhatsApp bot with various functions
-   There are various features available on Kιɳα Bσƚ
-   Kιɳα Bσƚ has a beautiful terminal logger
-   Full Installation Tutorial [Click Here](https://mega.nz/file/Qjs0mK5a#eHw6I57tqKks8H_7SJ3gLICY849801Hg3LxJuSIL2mw)

## Table of Contents

-   [Getting Started](#getting-started)
-   [Build With](#build_with)
-   [Installation](#installation)
-   [Documentation](#documentation)
-   [Community](#community)

## Getting Started

What is needed to run this project :

-   [GIT](https://git-scm.com/downloads)
-   [NodeJS version 16+](https://nodejs.org/en/)
-   [FFMPEG](https://ffmpeg.org/download.html)
-   [WEBP](https://storage.googleapis.com/downloads.webmproject.org/releases/webp/index.html)
-   You need a Chinese Proxy for the Image to Anime feature
-   You need the [OCR Space API KEY](https://ocr.space) to run the OCR feature

If you have problems, you can [open an issue](https://github.com/TobyG74/ChisatoBOT/issues) or join the community to ask questions about it

### Setup Your Mongodb

-   Login to the [MongoDB](https://account.mongodb.com/account/login) website
-   Create your Database
-   Next, select the Database that you created again or click (Database > Connect > Drivers > Copy Your Application Code)
-   Paste the mongodb code that you copied into the .env file and don't forget to change `<password>` to your database password

### Setup Your `.env` File

-   Edit your [.env](https://github.com/TobyG74/ChisatoBOT/blob/master/.env.example) file
-   Rename `.env.example` to `.env`

## Built With

![TypeScript](https://img.shields.io/badge/TypeScript-2F6BA3?style=for-the-badge&logo=typescript&logoColor=FFFFFF)
![Prisma](https://img.shields.io/badge/prisma-29245c?style=for-the-badge&logo=prisma&logoColor=F7DF1E)
![MongoDB](https://img.shields.io/badge/MongoDB-FFFFFF?style=for-the-badge&logo=mongodb&logoColor=2FA331)

## Installation

### Clone this Project

```
git clone https://github.com/ikyalwaysgood/Simple-Bot
cd Simple-Bot
```

### Install Dependencies

```
npm install
```

### Setup Prisma

```
npx prisma db push
```

### Build Project

```
npm run build
```

### Run Project

-   Run with PM2

```
npm run pm2:start
```

-   Without PM2

```
npm start
```

---

## Documentation

### Configuration File [config.json](https://github.com/TobyG74/ChisatoBOT/blob/master/config.json)

-   `ownerNotifyOnline` to send a message to the Owner whenever the Bot is Online
-   `useLimit` for limit configuration, if `true` then every time the command will use the limit
-   `useCooldown` for cooldown configuration, if `true` then every time the command will use the cooldown

```json
{
    "ownerNumber": ["YOUR_NUMBER"],
    "teamNumber": [],
    "timeZone": "Asia/Jakarta",
    "prefix": ".",
    "maintenance": [], // List Maintenance Command
    "stickers": {
        "author": "Instagram : iky_alwaysgood",
        "packname": "Made by Iky𝖔𝖋𝖋𝖎𝖈𝖎𝖆𝖑ཽ"
    },
    "settings": {
        "ownerNotifyOnline": false,
        "selfbot": false,
        "useLimit": false,
        "useCooldown": true,
        "autoReadMessage": true,
        "autoReadStatus": true
    },
    "call": {
        "status": "reject" // reject, block, off
    },
    "limit": {
        "command": 30
    },
    "cfonts": {
        "font": "block",
        "align": "center",
        "colors": ["green", "yellow"],
        "background": "transparent",
        "letterSpacing": 0,
        "lineHeight": 0,
        "space": true,
        "maxLength": "0",
        "gradient": false,
        "independentGradient": false,
        "transitionGradient": false,
        "env": "node"
    }
}
```

### Config Commands

-   Command configuration that you can use

```ts
type ConfigCommands = {
    name: string;
    alias: string[];
    usage: string;
    category: string;
    description: string;
    cooldown?: number; // in seconds
    limit?: number;
    example?: string;
    isOwner?: boolean;
    isTeam?: boolean;
    isPrivate?: boolean;
    isPremium?: boolean;
    isGroup?: boolean;
    isGroupAdmin?: boolean;
    isGroupOwner?: boolean;
    isBotAdmin?: boolean;
    isProcess?: boolean;
    run: (args: CommandsObject) => unknown;
};
```

