# Laravel and Filament package guidance

Read README.md, the [Filament standard](https://github.com/liberusoftware/documentation/blob/main/standards/FILAMENT.md) and [module architecture](https://github.com/liberusoftware/documentation/blob/main/architecture/MODULES.md).

- Keep explicit plugin registration and independent Composer metadata. Reusable packages must not depend on host App namespaces.
- Keep canonical Laravel owners authoritative for policy, tenant context, rules, transactions and persistence. Present authorized results through the module's public boundary.
- Add only capability-specific resources, pages and widgets. Do not copy domain records or enable unrelated modules.
- Validate Composer metadata, PHP syntax and the plugin contract in a compatible consumer. Add meaningful authorization/journey tests as real behavior is implemented.
- Keep skeleton status until integration is verified. Do not publish to Packagist or deploy applications without task authorization.
