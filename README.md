<div align="center">

# Hi, I'm Sepehr Imanian 👋

<img src="https://komarev.com/ghpvc/?username=SepehrImanian&style=flat-square&color=blue" alt="Profile views"/>

**Senior Platform Engineer & DevOps Lead · 8+ Years · Kubernetes · Go · eBPF**

I build platform infrastructure for high-traffic systems serving 20M+ users — custom Kubernetes operators in Go, low-level Linux/eBPF security tooling, and Internal Developer Platforms that cut cloud overhead and accelerate delivery. Open source contributor to the Terraform and Cisco ecosystems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sep-imanian/)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sepehrimaniann@gmail.com)

</div>

---

## Skills

**Languages**

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

**Kubernetes & Cloud Native**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)
![Linkerd](https://img.shields.io/badge/Linkerd-2BEDA7?style=flat-square&logo=linkerd&logoColor=black)
![Cilium](https://img.shields.io/badge/Cilium-F8C517?style=flat-square&logo=cilium&logoColor=black)

Custom operators · admission webhooks · CRDs · HPA/VPA/KEDA · Kubebuilder / controller-runtime

**eBPF & Linux Internals**

![eBPF](https://img.shields.io/badge/eBPF-F6931B?style=flat-square&logo=linux&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

Tetragon · bpftrace · libbpf · kprobes/uprobes · cgroups v2 · namespaces · kernel tuning (sysctl, NUMA, CPU scheduler) · TCP/IP internals (conntrack, TIME_WAIT, BBR, BIG TCP)

**Platform Engineering**

![Backstage](https://img.shields.io/badge/Backstage-9BF0E1?style=flat-square&logo=backstage&logoColor=black)
![Crossplane](https://img.shields.io/badge/Crossplane-EF7B4D?style=flat-square&logo=crossplane&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)

Thanos · VictoriaMetrics · Alertmanager · EFK Stack · custom eBPF probes

**Security & Networking**

![HAProxy](https://img.shields.io/badge/HAProxy-1188D7?style=flat-square&logo=haproxy&logoColor=white)

Tetragon (eBPF) · DevSecOps (Semgrep, Trivy, Grype, Syft) · Keycloak · OAuth2-Proxy · ModSecurity · Teleport  
BGP · VXLAN · netfilter/nftables · L4/L7 load balancing (HAProxy, Nginx, Envoy) · CCNA/CCNP

---

## Projects

### Kubernetes Operators & Controllers

- [**ip-pool-operator**](https://github.com/SepehrImanian/ip-pool-operator) — Kubernetes operator that auto-syncs remote IP/CIDR allowlists (CDNs, cloud providers) into `NetworkPolicy` resources
  - Fetches IP ranges from external URLs on a configurable interval (default: 1h) with deduplication and `#`-comment handling
  - Flexible namespace targeting via label selectors; supports Ingress/Egress with port/protocol control
  - Multi-architecture images (linux/amd64, linux/arm64); built on Kubebuilder / controller-runtime
  - Supports providers like Cloudflare, Arvan Cloud, bunny.net, and Sotoon out of the box

### Networking & System Daemons

- [**glbp**](https://github.com/SepehrImanian/glbp) — Linux daemon (Go) implementing GLBP-inspired gateway load balancing with virtual IP election and rotating virtual MACs
  - Multicast UDP hello protocol with priority-based AVG election and optional preemption
  - Round-robin ARP MAC distribution to spread client connections across multiple routers
  - Uses libpcap for ARP I/O; YAML-based config with configurable hello/hold timers

### Terraform Providers

- [**terraform-provider-haproxy**](https://github.com/SepehrImanian/terraform-provider-haproxy) — Terraform provider for managing HAProxy configuration
  - End-to-end, unit, and integration test suite
  - Supports runtime changes and configuration validation

### Observability

- [**s3-ceph-exporter**](https://github.com/SepehrImanian/s3-ceph-exporter) — Prometheus exporter for monitoring Ceph RGW / S3
  - Grafana dashboards included
  - End-to-end, unit, and integration tests

### Ansible Playbooks & Roles

- [**ansible-role-haproxy**](https://github.com/AvengersOfAutomations/ansible-role-haproxy) — Ansible role for HAProxy + Keepalived + Data Plane API
  - Multi-instance HAProxy with Keepalived; idempotent execution; fully customizable
- [**ansible-etcd-cluster**](https://github.com/SepehrImanian/ansible-etcd-cluster) — Etcd cluster setup with or without TLS; includes a dedicated teardown role
- [**ansible-hadoop-hdfs**](https://github.com/SepehrImanian/ansible-hadoop-hdfs) — Hadoop HDFS cluster automation with disk/DNS management and safe cluster teardown

### Tutorials & Learning Resources

- [**kafka-docs**](https://github.com/SepehrImanian/kafka-docs) — Apache Kafka reference documentation from fundamentals to advanced patterns
  - Covers Kafka concepts, CLI tooling, producer/consumer implementation, and advanced topics
  - Structured progressively for developers at any level
- [**ansible-tutorial**](https://github.com/SepehrImanian/ansible-tutorial) — Step-by-step Ansible guide with practical examples and best practices
- [**Linkerd-Flagger-Tutorial**](https://github.com/SepehrImanian/Linkerd-Flagger-Tutorial.git) — Linkerd & Flagger integration tutorial with troubleshooting tips
