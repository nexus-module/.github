# Terraform Nexus Modules

Comprehensive Terraform modules for Sonatype Nexus Repository Manager configuration.

## Available Modules

| Module | Description | Registry |
|--------|-------------|----------|
| terraform-nexus-security | Security settings (LDAP, users, roles, content selectors) | [Registry](https://registry.terraform.io/modules/nexus-module/security/nexus) |
| terraform-nexus-repository | Repository management (40+ types: hosted, proxy, group) | [Registry](https://registry.terraform.io/modules/nexus-module/repository/nexus) |
| terraform-nexus-blobstore | Blob storage configuration | [Registry](https://registry.terraform.io/modules/nexus-module/blobstore/nexus) |
| terraform-nexus-routing | Routing rules | [Registry](https://registry.terraform.io/modules/nexus-module/routing/nexus) |
| terraform-nexus-privilege | Access privileges management | [Registry](https://registry.terraform.io/modules/nexus-module/privilege/nexus) |
| terraform-nexus-script | Groovy script deployment | [Registry](https://registry.terraform.io/modules/nexus-module/script/nexus) |
| terraform-nexus-mail | Email server configuration | [Registry](https://registry.terraform.io/modules/nexus-module/mail/nexus) |

All modules use the [Nexus Provider](https://registry.terraform.io/providers/datadrivers/nexus) (datadrivers/nexus).

## Maintainers

| Name |
| ---- |
| [ialejandro](https://github.com/ialejandro) |
| [amartingarcia](https://github.com/amartingarcia) |

## Get Involved

We welcome contributions from the community. Feel free to open issues, submit pull requests, and join the discussions in our repositories. Together, we can build better tools and make the DevOps community stronger.

## License

All our projects are released under the [MIT License](../LICENSE).
