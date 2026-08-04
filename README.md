# wasmCloud

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

wasmCloud is a CNCF incubating platform for building, managing, and scaling distributed applications using WebAssembly components. It provides a runtime that manages the lifecycle of WebAssembly actors and capability providers, enabling developers to write portable business logic that connects to infrastructure capabilities like HTTP servers, messaging, key-value stores, and databases through a declarative linking model based on WebAssembly Interface Types (WIT).

**Website:** https://wasmcloud.com  
**Documentation:** https://wasmcloud.com/docs/  
**GitHub:** https://github.com/wasmCloud  
**Community:** https://slack.wasmcloud.com/  
**APIs.json:** https://raw.githubusercontent.com/api-evangelist/wasmcloud/refs/heads/main/apis.yml

## Tags

Cloud Native, CNCF, Distributed Systems, Incubating, Kubernetes, Runtime, Wasm, WebAssembly, WIT

---

## APIs

### wasmCloud Control Interface API

NATS-based control plane API for managing the wasmCloud lattice — starting/stopping components and providers, managing link definitions, scaling applications, and querying host inventories.

- **Documentation:** https://wasmcloud.com/docs/hosts/lattice-protocols/control-interface/
- **AsyncAPI:** [asyncapi/wasmcloud-control-asyncapi.yml](asyncapi/wasmcloud-control-asyncapi.yml)
- **AsyncAPI:** [asyncapi/wasmcloud-lattice-events-asyncapi.yml](asyncapi/wasmcloud-lattice-events-asyncapi.yml)

### wasmCloud Application Deployment Manager (wadm) API

Declarative GitOps API for managing wasmCloud application deployments using OAM manifests. wadm reconciles desired state across the lattice.

- **Documentation:** https://wasmcloud.com/docs/ecosystem/wadm/
- **AsyncAPI:** [asyncapi/wasmcloud-wadm-asyncapi.yml](asyncapi/wasmcloud-wadm-asyncapi.yml)
- **JSON Schema:** [json-schema/wasmcloud-manifest-schema.json](json-schema/wasmcloud-manifest-schema.json)
- **JSON Schema:** [json-schema/wasmcloud-oam-manifest-schema.json](json-schema/wasmcloud-oam-manifest-schema.json)

### wasmCloud wash CLI

Primary command-line tool for developing, building, deploying, and managing wasmCloud applications. Bundles a local wasmCloud host, NATS server, and wadm.

- **Documentation:** https://wasmcloud.com/docs/cli/wash/
- **GitHub:** https://github.com/wasmCloud/wash

### wasmCloud WIT Interfaces

WebAssembly Interface Type definitions for wasmCloud capability providers covering WASI 0.2 and wasmCloud-specific interfaces.

- **Documentation:** https://wasmcloud.com/docs/concepts/interfaces/
- **GitHub:** https://github.com/wasmCloud/wasmCloud

### wasmCloud Kubernetes Operator

Kubernetes operator for running wasmCloud infrastructure natively on Kubernetes clusters. Defines CRDs for Hosts, Artifacts, Workloads, WorkloadDeployments, and WorkloadReplicaSets under the `runtime.wasmcloud.dev` group.

- **Documentation:** https://wasmcloud.com/docs/deployment/k8s/
- **GitHub:** https://github.com/wasmCloud/wasmcloud-operator

---

## Artifacts

### AsyncAPI Specifications

| File | Description |
|------|-------------|
| [asyncapi/wasmcloud-control-asyncapi.yml](asyncapi/wasmcloud-control-asyncapi.yml) | Control Interface API — NATS subjects for host management |
| [asyncapi/wasmcloud-wadm-asyncapi.yml](asyncapi/wasmcloud-wadm-asyncapi.yml) | wadm Application Deployment Manager API |
| [asyncapi/wasmcloud-lattice-events-asyncapi.yml](asyncapi/wasmcloud-lattice-events-asyncapi.yml) | Host lifecycle event stream |

### JSON Schemas

| File | Description |
|------|-------------|
| [json-schema/wasmcloud-manifest-schema.json](json-schema/wasmcloud-manifest-schema.json) | wasmCloud OAM application manifest schema |
| [json-schema/wasmcloud-oam-manifest-schema.json](json-schema/wasmcloud-oam-manifest-schema.json) | Full OAM manifest schema with component traits |

### JSON Structures

| File | Description |
|------|-------------|
| [json-structure/wasmcloud-oam-manifest-structure.json](json-structure/wasmcloud-oam-manifest-structure.json) | OAM manifest field structure documentation |

### JSON-LD Contexts

| File | Description |
|------|-------------|
| [json-ld/wasmcloud-context.jsonld](json-ld/wasmcloud-context.jsonld) | JSON-LD context mapping wasmCloud vocabulary to schema.org and WASM ontologies |

### Examples

| File | Description |
|------|-------------|
| [examples/wasmcloud-oam-manifest-example.json](examples/wasmcloud-oam-manifest-example.json) | Hello World application OAM manifest |
| [examples/wasmcloud-scale-component-example.json](examples/wasmcloud-scale-component-example.json) | Control interface scale component command |
| [examples/wasmcloud-link-definition-example.json](examples/wasmcloud-link-definition-example.json) | Link definition connecting component to provider |

### Vocabulary

| File | Description |
|------|-------------|
| [vocabulary/wasmcloud-vocabulary.yml](vocabulary/wasmcloud-vocabulary.yml) | Domain vocabulary: Lattice, Component, Provider, WIT, WASI, NKey, wadm, wash |

### Kubernetes CRDs

| File | Kind | Group |
|------|------|-------|
| [crd/runtime.wasmcloud.dev_hosts.yaml](crd/runtime.wasmcloud.dev_hosts.yaml) | Host | runtime.wasmcloud.dev |
| [crd/runtime.wasmcloud.dev_artifacts.yaml](crd/runtime.wasmcloud.dev_artifacts.yaml) | Artifact | runtime.wasmcloud.dev |
| [crd/runtime.wasmcloud.dev_workloads.yaml](crd/runtime.wasmcloud.dev_workloads.yaml) | Workload | runtime.wasmcloud.dev |
| [crd/runtime.wasmcloud.dev_workloaddeployments.yaml](crd/runtime.wasmcloud.dev_workloaddeployments.yaml) | WorkloadDeployment | runtime.wasmcloud.dev |
| [crd/runtime.wasmcloud.dev_workloadreplicasets.yaml](crd/runtime.wasmcloud.dev_workloadreplicasets.yaml) | WorkloadReplicaSet | runtime.wasmcloud.dev |

---

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com
