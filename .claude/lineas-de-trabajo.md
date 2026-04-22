# Líneas de trabajo — Legion Cloud

> Áreas concretas con **referencias contrastables** (libros, whitepapers oficiales, frameworks, industria) como punto de partida del equipo.
>
> Ver definición de estados en `../../templates/lineas-de-trabajo.md.template`.

---

## Líneas activas

(Ninguna todavía — división arranca en 2026-04.)

---

## Líneas en exploración / diseño

### Data Platform Services

- **Estado:** `designing`
- **Objetivo:** servicio ancla. Diseño e implementación de data platforms modernas (batch + streaming + analytics).
- **Motivación:** área donde Fabio y equipo inicial tienen mayor experiencia. Ticket atractivo. Ciclo de venta razonable.
- **Siguiente paso:** escribir blueprint público (architecture + tooling recomendado) y un playbook de discovery.

**Referencias:**

*Libros:*
- Reis & Housley, *Fundamentals of Data Engineering* (O'Reilly, 2022). **Marco canónico** del data engineering lifecycle.
- Dehghani, *Data Mesh: Delivering Data-Driven Value at Scale* (O'Reilly, 2022). Texto fundacional del paradigma.
- Kimball & Ross, *The Data Warehouse Toolkit* (Wiley, 3rd ed. 2013). Modelado dimensional; vigente.
- Zburivsky & Partner, *Designing Cloud Data Platforms* (Manning, 2021).

*Whitepapers / docs:*
- [Databricks Lakehouse paper (CIDR 2021)](https://www.cidrdb.org/cidr2021/papers/cidr2021_paper17.pdf) — arquitectura Lakehouse original.
- [Medallion architecture — Databricks docs](https://docs.databricks.com/aws/en/lakehouse/medallion).
- [Data Mesh on Google Cloud](https://cloud.google.com/architecture/data-mesh).
- [Dehghani — Data Monolith to Mesh (martinfowler.com)](https://martinfowler.com/articles/data-monolith-to-mesh.html). El post original.

*Stack (open-source + SaaS):*
- **dbt** — [getdbt.com](https://www.getdbt.com). Transformaciones SQL.
- **Airflow / Dagster / Prefect** — orquestación.
- **Airbyte / Fivetran** — ingesta/CDC.
- **Kafka + Flink** — streaming.
- **Delta Lake / Apache Iceberg / Apache Hudi** — open table formats.
- Plataformas: Snowflake, Databricks, BigQuery, Microsoft Fabric, ClickHouse.

*Conferencias / industria:*
- Google Cloud Next ("Data & AI" track), Data + AI Summit (Databricks), Snowflake Summit, Airflow Summit.
- LakeFS "State of Data Engineering" report anual.
- ThoughtWorks "Data Mesh in Practice".

*Por dónde empezar:*
- Reis & Housley (cap 1-3) para vocabulario compartido.
- Medallion docs Databricks como patrón de ejecución default.

---

### Cloud Migration (AWS / GCP / Azure)

- **Estado:** `designing`
- **Objetivo:** servicio ancla con metodología 6R (rehost / replatform / refactor / repurchase / retire / retain).
- **Motivación:** demanda regional alta, ticket alto.
- **Siguiente paso:** metodología + entregables estándar + pricing orientativo.

**Referencias:**

*Libros:*
- Laszewski & Nauduri, *Migrating to the Cloud* (Syngress/Elsevier). Canónico para planificación enterprise.
- Piper & Clinton, *AWS Certified Solutions Architect Study Guide* (Sybex, 2023). Cubre 6R y CAF operativamente.
- Abdula et al., *Cloud Adoption Playbook* (Wiley). Marco vendor-neutral.

*Whitepapers / docs oficiales (obligados):*
- [AWS Cloud Adoption Framework (PDF)](https://docs.aws.amazon.com/pdfs/whitepapers/latest/overview-aws-cloud-adoption-framework/overview-aws-cloud-adoption-framework.pdf).
- [Azure Cloud Adoption Framework](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/).
- [Google Cloud Adoption Framework (whitepaper)](https://services.google.com/fh/files/misc/google_cloud_adoption_framework_whitepaper.pdf).
- [Google "Understanding Cloud Migration Frameworks"](https://cloud.google.com/resources/understanding-cloud-migration-frameworks-whitepaper).
- [AWS Well-Architected Migration Lens](https://docs.aws.amazon.com/wellarchitected/latest/migration-lens/).

*Tooling:*
- [AWS Migration Hub](https://aws.amazon.com/migration-hub/).
- [Azure Migrate](https://azure.microsoft.com/en-us/products/azure-migrate/).
- [Google Cloud Migration Center](https://cloud.google.com/migration-center).

*Conferencias / industria:*
- AWS re:Invent "Migration & Modernization" track.
- Gartner "Magic Quadrant for Public Cloud IT Transformation Services".

*Por dónde empezar:*
- AWS CAF Overview + Azure CAF "Plan your migration" — las dos taxonomías dominantes.

---

### Cloud Architecture Review

- **Estado:** `designing`
- **Objetivo:** auditoría + roadmap de mejora basado en Well-Architected Frameworks (AWS 6 pilares / Azure 5 / GCP).
- **Motivación:** servicio de alta conversión (cliente paga auditoría → engagement más grande).
- **Siguiente paso:** checklist + entregable estándar + precio fijo.

**Referencias:**

*Libros:*
- Kleppmann & Riccomini, *Designing Data-Intensive Applications*, 2nd ed. (O'Reilly, 2026). **Base canónica** de sistemas distribuidos.
- Ford, Richards, Sadalage, Dehghani, *Software Architecture: The Hard Parts* (O'Reilly, 2021). Trade-offs en distribuidos modernos.
- Richards & Ford, *Fundamentals of Software Architecture* (O'Reilly, 2020). Precursor del anterior.

*Whitepapers / docs oficiales:*
- [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/) — 6 pilares.
- [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/) — 5 pilares.
- [Google Cloud Well-Architected](https://cloud.google.com/architecture/framework).
- [AWS Prescriptive Guidance Patterns](https://docs.aws.amazon.com/prescriptive-guidance/).

*Frameworks / catálogos:*
- [Azure Architecture Center (patrones)](https://learn.microsoft.com/en-us/azure/architecture/patterns/).
- [Google Cloud Architecture Center](https://cloud.google.com/architecture).
- [AWS Solutions Library](https://aws.amazon.com/solutions/).
- [AWS Well-Architected Tool](https://aws.amazon.com/well-architected-tool/) — self-assessment.

*Conferencias / industria:*
- AWS re:Invent "Architecture" track.
- ThoughtWorks Technology Radar (semestral) — benchmark de patrones emergentes.

*Por dónde empezar:*
- AWS Well-Architected Framework (el vocabulario compartido de la industria).
- Kleppmann cap 1-4 para fundamentos.

---

### FinOps

- **Estado:** `exploring`
- **Objetivo:** optimización sistemática de costos cloud con metodología FinOps Foundation.
- **Motivación:** pain point universal post-migración. Ticket bajo pero recurrente (retainer-friendly).
- **Siguiente paso:** decidir si es servicio standalone o add-on. Diseñar "Cost Review" de 2 semanas como producto.

**Referencias:**

*Libros:*
- Storment & Fuller, *Cloud FinOps*, 2nd ed. (O'Reilly, 2023). **Biblia de la disciplina**, escrita por liderazgo de la FinOps Foundation.
- Milanese, *FinOps: A New Approach to Cloud Financial Management* (Apress, 2024).

*Frameworks / estándares:*
- [FinOps Framework](https://www.finops.org/framework/) — fases + capabilities + scopes.
- [FOCUS 1.0 Specification](https://focus.finops.org/focus-specification/v1-0/) — FinOps Open Cost and Usage Spec. **Lectura obligada 2025+.**
- [Microsoft FinOps guide](https://learn.microsoft.com/en-us/cloud-computing/finops/).

*Open-source:*
- [OpenCost](https://www.opencost.io/) (CNCF) — cost allocation K8s.
- [Kubecost](https://www.kubecost.com/).
- [Infracost](https://www.infracost.io/) — cost diffs en CI/CD.
- [Karpenter](https://karpenter.sh/) — autoscaler AWS eficiente.

*Herramientas comerciales referencia:*
- CloudHealth (VMware), Apptio Cloudability, Vantage, Cast.ai, Spot.io (NetApp), ProsperOps.

*Conferencias / reportes:*
- [FinOps X](https://x.finops.org/) — conferencia anual de la Foundation.
- [State of FinOps Report](https://data.finops.org/) — anual.

*Por dónde empezar:*
- *Cloud FinOps 2nd ed.* (cap 1-6).
- FinOps Framework overview en finops.org.

---

### Platform Engineering / DevOps

- **Estado:** `exploring`
- **Objetivo:** plataformas internas, IaC, CI/CD, golden paths.
- **Motivación:** empresas medianas lo piden frecuentemente.
- **Siguiente paso:** definir reference architectures (Kubernetes-based, serverless-based).

**Referencias:**

*Libros:*
- Skelton & Pais, *Team Topologies* (IT Revolution, 2019; 2nd ed. 2025). **Fundamento organizativo**.
- Fournier & Nowland, *Platform Engineering* (O'Reilly, 2024). Texto de referencia actual.
- Forsgren, Humble & Kim, *Accelerate* (IT Revolution, 2018). Base científica DORA.
- Kim et al., *The Phoenix Project* (IT Revolution). Narrativa canónica.
- Kim, Humble, Debois, Willis, Forsgren, *The DevOps Handbook*, 2nd ed. (2021). Manual práctico.

*Whitepapers / reports:*
- [DORA 2024 Accelerate State of DevOps Report](https://dora.dev/research/2024/dora-report/) ([PDF](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf)).
- [CNCF Platforms White Paper](https://tag-app-delivery.cncf.io/whitepapers/platforms/).
- [SPACE Framework (ACM Queue)](https://queue.acm.org/detail.cfm?id=3454124) — Forsgren et al.
- [OpenTelemetry spec](https://opentelemetry.io/docs/specs/).

*Frameworks / open-source:*
- [CNCF Landscape](https://landscape.cncf.io/) — mapa completo del ecosistema.
- [Backstage](https://backstage.io/) — Internal Developer Platform (Spotify-born).
- [ArgoCD](https://argo-cd.readthedocs.io/) / [FluxCD](https://fluxcd.io/) — GitOps.
- [Crossplane](https://www.crossplane.io/) — control plane.
- [Istio](https://istio.io/) / [Linkerd](https://linkerd.io/) — service mesh.
- [Dapr](https://dapr.io/) — distributed app runtime.
- [OpenTelemetry](https://opentelemetry.io/) — observability estándar.

*Conferencias / industria:*
- DORA Report anual (Google Cloud).
- [PlatformCon](https://platformcon.com/) — conferencia anual, platformengineering.org.
- KubeCon + CloudNativeCon (CNCF).
- Reportes GetDX sobre developer experience.

*Golden triangle IDP 2024-2025:* Backstage + ArgoCD + Crossplane.

*Por dónde empezar:*
- *Team Topologies* para lenguaje organizativo.
- DORA 2024 Report para métricas y benchmarks (lo que cualquier stakeholder del cliente reconoce).

---

## Líneas en exploración (sin refs aún)

### Staff augmentation senior

- **Estado:** `idea`
- **Objetivo:** consultor senior integrado temporalmente en equipo cliente.
- **Siguiente paso:** decidir si existe como Cloud o como Legion Staffing (división separada).

### Thought leadership / content marketing

- **Estado:** `exploring`
- **Objetivo:** contenido técnico regular para demanda orgánica.
- **Siguiente paso:** calendario; primer artículo ancla (data platform blueprint).

---

## Líneas archivadas

(Vacío.)

---

## Core reading cross-línea (5 libros)

Con estos cinco, un consultor senior tiene vocabulario para operar en las 5 líneas:

1. Kleppmann — *Designing Data-Intensive Applications*
2. Reis & Housley — *Fundamentals of Data Engineering*
3. Storment & Fuller — *Cloud FinOps*
4. Skelton & Pais — *Team Topologies*
5. Fournier & Nowland — *Platform Engineering*

## Conferencias anuales a seguir

AWS re:Invent · Google Cloud Next · Microsoft Ignite · KubeCon · FinOps X · Data+AI Summit · PlatformCon.

## Reportes recurrentes (citables en propuestas)

DORA State of DevOps · State of FinOps · ThoughtWorks Technology Radar · CNCF Annual Survey.

---

**Última actualización:** 2026-04-22
