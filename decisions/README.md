# Decisiones

Este directorio contiene las decisiones institucionales relevantes de Orvental.

Una decisión debe permitir reconstruir:

> **qué se decidió, por qué, con qué evidencia, quién fue responsable y qué ocurrió después.**

El objetivo no es registrar cada decisión cotidiana, sino conservar aquellas que puedan afectar la estrategia, operación, metodología, tecnología o dirección de Orvental.

---

## Principios

* Las decisiones importantes deben quedar versionadas en Git.
* Las decisiones deben basarse, cuando sea posible, en evidencia documentada.
* Una decisión puede cambiar cuando aparece nueva evidencia.
* Las decisiones reemplazadas no se eliminan; se conservan para mantener trazabilidad histórica.
* La responsabilidad de una decisión permanece en la persona responsable, aunque posteriormente se utilicen herramientas de IA para asistir el análisis.
* No se debe convertir el sistema en burocracia: registrar lo que tenga valor institucional.

---

## Identificación

Cada decisión utiliza un identificador estable:

```text
DEC-001
DEC-002
DEC-003
```

Los documentos utilizan:

```text
YYYY-MM-DD-short-description.md
```

Ejemplo:

```text
2026-09-30-git-as-source-of-truth.md
```

El identificador `DEC-XXX` permanece estable aunque posteriormente cambie el estado de la decisión.

---

## Estados

Una decisión puede tener uno de estos estados:

```text
Proposed
Accepted
Rejected
Superseded
```

### Proposed

La decisión está siendo evaluada y todavía no es institucional.

### Accepted

La decisión fue adoptada y representa la posición vigente de Orvental.

### Rejected

La alternativa fue evaluada y descartada.

### Superseded

La decisión fue reemplazada por una decisión posterior.

La decisión original debe permanecer en Git para conservar el historial.

---

## Plantilla

Crear cada decisión utilizando esta estructura:

```markdown
# DEC-XXX — Título de la decisión

**Fecha:** YYYY-MM-DD
**Estado:** Proposed | Accepted | Rejected | Superseded
**Responsable:** Nombre
**Área:** strategy | sales | research | sop | technology | other

## Contexto

¿Qué situación, problema u oportunidad requiere una decisión?

## Pregunta

¿Qué necesitamos decidir?

## Opciones consideradas

### Opción A

Descripción breve.

### Opción B

Descripción breve.

### Opción C

Descripción breve, si aplica.

## Decisión

¿Qué se decidió?

## Razones

¿Por qué se tomó esta decisión?

Separar hechos observados de supuestos o interpretaciones.

## Evidencia

Registrar la evidencia utilizada.

Puede incluir referencias a:

- experimentos;
- métricas;
- resultados comerciales;
- documentos;
- investigaciones;
- feedback de clientes;
- incidentes;
- experiencias operativas.

Ejemplo:

- EXP-003
- Métrica de conversión de septiembre
- Discovery con cliente X

## Consecuencias

¿Qué cambia como resultado de esta decisión?

### Positivas

-

### Negativas / trade-offs

-

### Riesgos

-

## Resultado

Completar posteriormente cuando exista evidencia suficiente.

¿Qué ocurrió después de implementar la decisión?

## Revisión

¿Qué condición, fecha o nueva evidencia debería provocar una revisión?

## Decisiones relacionadas

- DEC-XXX
- DEC-XXX
```

---

## Evidencia y experimentos

Cuando una decisión se base en un experimento, debe existir una referencia al experimento correspondiente:

```text
DEC-004
    ↓
EXP-007
    ↓
Resultado
```

Cuando un experimento produzca un aprendizaje que cambie una decisión institucional, la relación debe documentarse en ambos sentidos cuando sea útil.

Esto permite construir una cadena de trazabilidad:

```text
Hipótesis
    ↓
Experimento
    ↓
Evidencia
    ↓
Decisión
    ↓
Implementación
    ↓
Resultado
    ↓
Nueva evidencia
```

---

## Decisiones asistidas por IA

Orvental puede utilizar sistemas de inteligencia artificial para:

* recuperar contexto;
* resumir evidencia;
* identificar información relevante;
* comparar alternativas;
* detectar contradicciones;
* proponer preguntas;
* señalar riesgos;
* ayudar a evaluar escenarios.

La IA no constituye por sí misma la fuente de verdad.

Las decisiones institucionales deben poder reconstruirse a partir de sus documentos, evidencia y resultados registrados en Orvental OS.

La responsabilidad final de una decisión permanece en la persona responsable de dicha decisión.

---

## Preparación para Decision Intelligence

La estructura de este directorio debe permitir que, posteriormente, sistemas de IA puedan consultar de forma estructurada:

```text
decisiones
experimentos
evidencia
resultados
contexto
responsables
```

No se construirá un modelo de IA propio únicamente por anticipación.

Primero se construirá el sistema de conocimiento y evidencia.

Después se evaluará qué capacidades de inteligencia artificial aportan valor real.

---

## Reglas

1. No registrar decisiones triviales.
2. No borrar decisiones históricas relevantes.
3. No presentar opiniones como evidencia.
4. Diferenciar hechos, supuestos e interpretaciones.
5. Referenciar experimentos y datos cuando existan.
6. Registrar las consecuencias de las decisiones importantes.
7. Revisar decisiones cuando aparezca nueva evidencia relevante.
8. Mantener los documentos legibles por humanos y máquinas.
9. Evitar depender de funcionalidades propietarias de una herramienta.
10. Mantener Git como fuente de verdad institucional.
