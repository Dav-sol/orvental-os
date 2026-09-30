# Orvental OS

Sistema operativo institucional de Orvental.

Orvental OS conserva el conocimiento, las decisiones, metodologías, experimentos y procesos que deben sobrevivir independientemente de las herramientas utilizadas para ejecutar la operación.

## Principio fundamental

> Las herramientas ejecutan el sistema; Git conserva lo aprendido.

Plane, Twenty, n8n y Obsidian pueden cambiar.

El conocimiento institucional de Orvental debe permanecer.

---

## Arquitectura

Orvental OS separa **conocimiento, ejecución, relación comercial y automatización**.

### Git + Markdown — Fuente de verdad institucional

Git + Markdown es la fuente oficial del conocimiento institucional.

Aquí vive:

* estrategia;
* posicionamiento;
* ICP;
* ofertas;
* pricing;
* go-to-market;
* metodología comercial;
* investigación;
* experimentos;
* decisiones;
* SOPs;
* documentación que deba sobrevivir a cambios de herramientas.

El repositorio es portable y no depende de un proveedor específico.

### Obsidian — Interfaz de conocimiento

Obsidian es una interfaz de usuario sobre los archivos Markdown del repositorio.

Permite trabajar con el conocimiento de Orvental mediante una experiencia visual y accesible, especialmente para usuarios que no necesitan trabajar directamente con Git.

Obsidian **no es la fuente de verdad**.

Si Obsidian desaparece, el conocimiento continúa existiendo como Markdown dentro del repositorio Git.

La utilización de características específicas de Obsidian debe mantenerse limitada cuando puedan comprometer la portabilidad del conocimiento.

### Plane — Ejecución

Plane responde:

> ¿Qué estamos haciendo y quién lo está haciendo?

Aquí viven:

* proyectos;
* iniciativas;
* tareas;
* responsables;
* prioridades;
* ejecución operativa.

La estrategia completa no debe duplicarse en Plane.

### Twenty — CRM

Twenty es la memoria comercial viva de Orvental.

Aquí viven:

* empresas;
* contactos;
* leads;
* oportunidades;
* etapas comerciales;
* próximos pasos;
* información de discovery;
* actividad comercial.

Twenty representa el **estado actual de la operación comercial**.

### n8n — Automatización

n8n conecta y automatiza procesos entre los sistemas.

Durante v0.1 se prioriza comprender y estandarizar los procesos manuales antes de automatizarlos.

No se deben automatizar procesos que todavía no comprendemos suficientemente.

### Acceso privado — Infraestructura

Los sistemas internos de Orvental se mantienen privados durante v0.1.

El acceso se gestiona mediante una red privada autorizada. La implementación actual utiliza Tailscale.

La infraestructura puede migrar posteriormente de DaveCloud a un VPS o a otro proveedor sin modificar el conocimiento institucional.

---

## Estructura

```text
Orvental/
│
├── README.md
├── CONTRIBUTING.md
├── CHANGELOG.md
├── .gitignore
│
├── strategy/
│   ├── vision.md
│   ├── positioning.md
│   ├── icp.md
│   ├── offers.md
│   ├── pricing.md
│   └── go-to-market.md
│
├── sales/
│   ├── discovery.md
│   ├── qualification.md
│   └── messaging.md
│
├── research/
│   └── experiments.md
│
├── decisions/
│   └── README.md
│
└── sop/
    └── README.md
```

La estructura es deliberadamente modificable.

No se debe agregar complejidad antes de que exista una necesidad real.

---

## Sistema de aprendizaje

Orvental evoluciona mediante un ciclo explícito:

```text
Hipótesis
    ↓
Experimento
    ↓
Datos
    ↓
Aprendizaje
    ↓
Decisión
    ↓
Documentación
    ↓
Nueva hipótesis
```

Los experimentos se registran en `research/`.

Las decisiones relevantes se conservan en `decisions/`.

Los aprendizajes que cambien la estrategia, metodología u operación deben terminar documentados en el repositorio.

---

## Fuente de verdad

| Información                 | Fuente de verdad                          |
| --------------------------- | ----------------------------------------- |
| Estrategia                  | Git + Markdown                            |
| Decisiones                  | Git + Markdown                            |
| Metodologías                | Git + Markdown                            |
| SOPs                        | Git + Markdown                            |
| Documentación institucional | Git + Markdown                            |
| Interfaz de conocimiento    | Obsidian                                  |
| Proyectos                   | Plane                                     |
| Tareas                      | Plane                                     |
| Ejecución                   | Plane                                     |
| Leads                       | Twenty                                    |
| Contactos                   | Twenty                                    |
| Empresas                    | Twenty                                    |
| Oportunidades               | Twenty                                    |
| Clientes                    | Twenty                                    |
| Automatizaciones            | n8n                                       |
| Credenciales y secretos     | Gestor de secretos / variables de entorno |
| Acceso interno              | Red privada                               |

Las herramientas operativas no deben convertirse en el único lugar donde exista conocimiento crítico.

---

## Git y colaboración

`main` representa el conocimiento institucional aprobado.

El trabajo en progreso puede existir en ramas antes de integrarse.

```text
Working copy
     ↓
Commit
     ↓
Branch
     ↓
Review
     ↓
main
```

No todo cambio requiere una rama formal. La complejidad del flujo de Git debe mantenerse proporcional al tamaño del equipo y al riesgo del cambio.

Los cambios importantes de estrategia, procesos y decisiones deben quedar versionados.

---

## Portabilidad

Orvental OS no debe depender de una infraestructura, aplicación o proveedor específico.

Actualmente:

```text
DaveCloud
    ↓
Plane
Twenty
n8n
Git
Obsidian
```

Posteriormente puede convertirse en:

```text
VPS / Cloud
    ↓
Plane
Twenty
n8n
Git
Obsidian
```

El cambio de infraestructura no debe requerir reconstruir el conocimiento institucional.

---

## Regla v0.1

No buscamos construir el modelo perfecto de Orvental.

Buscamos aprender mediante clientes, experimentos y resultados reales.

La pregunta operativa principal es:

> ¿Qué hipótesis estamos probando esta semana?

Orvental OS debe evolucionar a partir de evidencia, no de complejidad anticipada.

---

## Principio de simplicidad

No construir todavía:

* ERP propio;
* portal de clientes;
* dashboard empresarial complejo;
* aplicación propia de Orvental;
* agentes autónomos complejos;
* automatizaciones innecesarias;
* infraestructura que no responda a una necesidad real.

Primero:

```text
Conseguir clientes
      ↓
Entender el proceso
      ↓
Estandarizar
      ↓
Medir
      ↓
Automatizar
      ↓
Aprender
      ↓
Mejorar
```

---

## Estado

**Versión:** v0.1
**Estado:** Foundation
**Propósito:** establecer el sistema institucional mínimo y portable de Orvental.

