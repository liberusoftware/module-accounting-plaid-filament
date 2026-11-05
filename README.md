# Laravel and Filament module foundation

An independent Composer package skeleton for a Filament panel extension. It supplies a plugin lifecycle entry with a unique ID. It registers no pages, resources, routes, policies or domain behavior yet.

## Develop

```bash
composer install
composer validate --strict
composer check
```

The application explicitly registers `Liberu\Presentation\BoilerplateFilament\BoilerplatePlugin::make()` in its panel provider's plugins list. No global auto-discovery enables this module. The package uses the Liberu module type; configure and allow the reviewed Liberu Composer installer in the consuming host to manage placement under `/modules`, following the [Composer lifecycle](https://github.com/liberusoftware/documentation/blob/main/guides/COMPOSER.md). Select compatible canonical core packages and invoke their public actions/queries from reviewed resources, pages and widgets. Installation, enablement, entitlement and authorization are separate responsibilities.

When deriving a capability, change the Composer identity, PSR-4 namespace, class/plugin ID and repository URL. Keep host `App\` imports and private model access outside the library. Implement and verify allowed/denied/wrong-tenant journeys before claiming a capability is delivered.

This repository is a template, not a published Packagist release. Read the [Filament standard](https://github.com/liberusoftware/documentation/blob/main/standards/FILAMENT.md), [module architecture](https://github.com/liberusoftware/documentation/blob/main/architecture/MODULES.md) and [source inventory](https://github.com/liberusoftware/documentation/blob/main/architecture/SOURCE-INVENTORY.md). Existing implementation packages retain their actual identities and remain separate from this skeleton.
