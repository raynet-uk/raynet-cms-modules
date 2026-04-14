# RAYNET CMS — Official Module Repository

<div align="center">

![RAYNET UK Logo](https://www.raynet-uk.net/technical/graphics/raynet-uk.gif)

**The official CMS platform for [RAYNET UK](https://www.raynet-uk.net) groups**

*Built for the Radio Amateurs' Emergency Network — by RAYNET Liverpool*

[![RAYNET UK](https://img.shields.io/badge/RAYNET-UK-003366?style=flat-square&labelColor=C8102E)](https://www.raynet-uk.net)
[![License](https://img.shields.io/badge/License-GPL--2.0-blue?style=flat-square)](https://www.gnu.org/licenses/gpl-2.0.html)
[![Platform](https://img.shields.io/badge/Platform-Laravel%2012-red?style=flat-square)](https://laravel.com)
[![PHP](https://img.shields.io/badge/PHP-8.2%2B-777BB4?style=flat-square)](https://php.net)

</div>

---

## What is RAYNET CMS?

RAYNET CMS is a web platform built specifically for **RAYNET UK** group websites. It is developed and maintained by [RAYNET Liverpool](https://raynet-liverpool.net) and is intended for use by RAYNET groups affiliated with [raynet-uk.net](https://www.raynet-uk.net).

> ⚠️ **This is not the same as other projects named "RAYNET CMS".** This platform is specifically designed for RAYNET UK groups and is built on Laravel 12. It is not affiliated with any other project of a similar name.

### Who is it for?

- ✅ RAYNET UK affiliated groups
- ✅ Groups registered at [raynet-uk.net](https://www.raynet-uk.net)
- ✅ Groups looking to replace a static or ageing website
- ✅ Groups wanting member management, event scheduling, and training tracking built in

### Who is it NOT for?

- ❌ Non-RAYNET organisations
- ❌ RACES, ARES, or other international emergency comms groups (though inspiration is welcome!)

---

## Features

- 📄 **Page Builder** — Visual page editor
- 👥 **Member Management** — registrations, roles, callsign verification
- 📅 **Event Management** — scheduling, RSVPs, operator assignments, briefings
- 🎓 **Training & LMS** — courses, quizzes, SCORM support, certificates
- 🔔 **Alert Status** — live RAYNET alert level display
- 📡 **Ops Map** — APRS, Meshtastic, weather and flood overlays
- 🔌 **Module System** — extend with modules, auto-updates from this repo
- 🔐 **SSO / OAuth** — single sign-on for connected tools

---

## Module Repository

This repository hosts official RAYNET CMS modules. Your CMS installation automatically checks here for updates via the Module Manager.

### Available Modules

| Module | Version | Description |
|--------|---------|-------------|
| TestWidget | 2.0.0 | Update system test module |

*More modules coming soon — Callout Log, Net Logger, Digital Membership Cards, and more.*

---

## For RAYNET Group Administrators

Your RAYNET CMS installation checks this repository automatically. To see available updates:

1. Log in to your admin panel
2. Go to **Module Manager**
3. Click **Check for Updates**

Updates are downloaded and applied with a single click — no FTP or server access required.

---

## Publishing a Module Update

*For RAYNET Liverpool maintainers only.*

1. Zip the updated module: `zip -r ModuleName-X.Y.Z.zip ModuleName/`
2. Create a GitHub Release tagged `module-name-X.Y.Z`
3. Upload the zip as a release asset
4. Edit `modules.json` — update `version`, `download_url`, `changelog`, `released_at`
5. Commit and push — all installed sites pick it up on next update check

### Module ZIP Structure

```
ModuleName/
├── module.json
├── Providers/
│   └── ModuleNameServiceProvider.php
├── Http/
│   └── Controllers/
├── Resources/
│   └── views/
└── Database/
    └── Migrations/
```

### module.json Required Fields

```json
{
    "name": "Human Readable Name",
    "alias": "module-alias",
    "version": "1.0.0",
    "description": "What this module does.",
    "author": "RAYNET Liverpool",
    "providers": ["Modules\\ModuleName\\Providers\\ModuleNameServiceProvider"]
}
```

---

## Links

- 🌐 [RAYNET UK](https://www.raynet-uk.net)
- 📻 [RAYNET Liverpool](https://raynet-liverpool.net)
- 📧 Contact: via [raynet-liverpool.net](https://raynet-liverpool.net/request-support)

---

<div align="center">
<sub>RAYNET CMS is developed by RAYNET Liverpool for the benefit of RAYNET UK groups.<br>
RAYNET is the Radio Amateurs' Emergency Network, affiliated with the RSGB.<br>
73 de RAYNET Liverpool 📻</sub>
</div>
