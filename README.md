# wasmCloud

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
