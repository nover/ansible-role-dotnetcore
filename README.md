# ansible role dotnet core

This role enables you to install one ore more dotnet SDKs on Ubuntu Trusty (14.04) and Xenial (16.04)

## Requirements

No pre-requisities are required for this package to work

## Role Variables

You can define one or more SDKs to install using this role, as Microsoft allows the SDKs to be installed side by side. 
The default is to install `dotnet-dev-1.0.4` which includes dotnet sdk and runtime 1.0.x and 1.1.x

To alter this, define your variable as

```yaml
dotnet_core_sdks:
  - dotnet-dev-1.0.4
  - dotnet-dev-2.0.0-preview1-005977
```

## Example Playbook

An example playbook for this role would be

```yaml
- hosts: all
  roles:
      - { 
          role: nover.dotnetcore,
          dotnet_core_sdks:
            - dotnet-dev-1.0.3
        }
```

## License

MIT

