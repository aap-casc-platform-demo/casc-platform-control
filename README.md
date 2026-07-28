# casc-platform-control

AAP CasC control plane: configuration, tenant registry, and naming policy

## Control Plane

This repository contains orchestration metadata only:

- `config.yml` — repository topology, environment branches, and Job Template names
- `tenants.yml` — tenant registry
- `naming-rules.yml.sample` — inert comprehensive naming-policy example covering cataloged `naming_supported` types (rename, adapt, and uncomment as `naming-rules.yml` to activate; never auto-activates)

Do not place AAP desired-state resource YAML in this repository. Use the
separate platform desired-state repository and its environment branches.

## CI/CD Pipeline

This repository includes a thin CI/CD caller that triggers the platform's
shared CasC pipeline on push and pull request events. The pipeline validates
YAML files and triggers the dispatcher Job Template in AAP.

## Part of the AAP Multi-Tenant CasC Framework

This repository is managed by the **aap-casc-platform-demo** platform team as part
of the AAP Multi-Tenant CasC Framework. See the
[aap-casc-engine](../aap-casc-engine) repository
for full documentation.
