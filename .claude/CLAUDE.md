# Legion Cloud — Contexto del repo

> Consultoría cloud: migración, arquitectura, FinOps, data platforms, DevOps.
>
> Parte de [Legion](../../CLAUDE.md) — holding de divisiones especializadas.

---

## 1. Qué es esta división

Legion Cloud es el brazo de **consultoría tecnológica** de Legion. Ayudamos a empresas a modernizar su stack cloud — desde migraciones hasta arquitecturas greenfield, FinOps, data platforms y DevOps. Inspiración operacional: Globant, Thoughtworks, Blue.

**Visibilidad:** Public. Este repo también sirve de vitrina para prospectos.

**Rol en Legion:** generador de ingresos por servicios profesionales. Cliente-facing. Público.

## 2. Referencias obligatorias

- [`../../CLAUDE.md`](../../CLAUDE.md) — contexto maestro de Legion
- [`../../team/git-workflow.md`](../../team/git-workflow.md) — convenciones Git
- [`../../team/claude-usage.md`](../../team/claude-usage.md) — cómo usar Claude Code
- [`./strategy.md`](./strategy.md) — estrategia de la división
- [`./lineas-de-trabajo.md`](./lineas-de-trabajo.md) — líneas activas

## 3. Stack técnico (por competencia)

Cubrimos los 3 grandes clouds con sesgo a profundidad en al menos dos:

```
Clouds:           AWS, GCP, Azure
IaC:              Terraform, OpenTofu, Pulumi
Data:             dbt, Airflow, BigQuery, Snowflake, Databricks, Kafka
DevOps:           GitHub Actions, GitLab CI, ArgoCD, FluxCD
Contenedores:     Docker, Kubernetes (EKS/GKE/AKS)
Observabilidad:   OpenTelemetry, Datadog, Grafana, Prometheus
Lenguajes:        Python, Go, TypeScript según proyecto
```

## 4. Estructura del repo (propuesta)

```
cloud/
├── .claude/
├── playbooks/            ← guías técnicas reutilizables (públicas)
├── blueprints/           ← referencias arquitectónicas (Terraform modules, reference apps)
├── case-studies/         ← casos públicos de clientes (con permiso)
├── blog/                 ← thought leadership
├── README.md
└── .gitignore
```

## 5. Convenciones locales

**Este repo es vitrina pública.** Todo lo que entra aquí se ve. Por tanto:

- **Cero información de clientes** sin autorización escrita.
- **Casos de estudio** se publican solo tras aprobación del cliente.
- **Blueprints y playbooks** deben ser genéricos y aplicables, no específicos a un cliente.
- El **README** es la primera impresión para prospects — cuidar copy y visuales.

**Trabajo específico de cliente:** va en repos privados separados (no en este), creados por engagement.

## 6. Co-authorship de Claude

Repo **public** → co-author Claude **permitido y recomendado** como señal de transparencia y dominio de la herramienta.

## 7. Contactos y responsables

- **Lead:** por definir
- **Equipo:** por formar (sr. cloud architect, data engineer, DevOps engineer)

## 8. Estado actual

Repo recién creado. Scaffold organizacional en curso. Líneas de servicio por definir con equipo antes de empezar marketing o ventas.
