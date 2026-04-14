# RAYNET CMS Modules

Official module repository for the RAYNET CMS platform.

## For RAYNET Groups

Your RAYNET CMS installation automatically checks this repository for updates.
No manual action required — updates appear in your Module Manager.

## modules.json

The `modules.json` file is the update manifest. Your CMS checks this file to
discover available module versions and download URLs.

## Publishing a Module Update (for maintainers)

1. Zip your updated module folder: `zip -r ModuleName-X.Y.Z.zip ModuleName/`
2. Create a GitHub Release tagged `module-name-X.Y.Z`
3. Upload the zip as a release asset
4. Edit `modules.json` — update `version`, `download_url`, `changelog`, `released_at`
5. Commit and push — all installed sites pick it up on next update check

## Module ZIP Structure

```
ModuleName/
├── module.json          (required — name, alias, version, description, providers)
├── Providers/
│   └── ModuleNameServiceProvider.php
├── Http/
│   └── Controllers/
├── Resources/
│   └── views/
└── Database/
    └── Migrations/
```

## module.json Required Fields

```json
{
    "name": "Human Readable Name",
    "alias": "module-alias",
    "version": "1.0.0",
    "description": "What this module does.",
    "author": "Your Name",
    "providers": ["Modules\\ModuleName\\Providers\\ModuleNameServiceProvider"]
}
```
