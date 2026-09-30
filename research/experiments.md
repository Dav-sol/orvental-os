# Experimentos

Este archivo registra experimentos utilizados para aprender sobre Orvental, sus clientes, mercado, procesos, ofertas y operaciones.

Un experimento convierte una hipótesis en una prueba observable.

## Principio

> No buscamos demostrar que una idea es correcta; buscamos obtener evidencia suficiente para decidir qué hacer después.

Ciclo:

```text
Hipótesis
    ↓
Experimento
    ↓
Acción
    ↓
Datos
    ↓
Resultado
    ↓
Aprendizaje
    ↓
Decisión
```

---

## Registro

| ID      | Fecha      | Hipótesis | Acción | Métrica | Resultado | Aprendizaje | Decisión | Estado  |
| ------- | ---------- | --------- | ------ | ------- | --------- | ----------- | -------- | ------- |
| EXP-001 | YYYY-MM-DD | ...       | ...    | ...     | ...       | ...         | ...      | Planned |

### Estados

* `Planned` — definido, aún no ejecutado.
* `Running` — actualmente en ejecución.
* `Completed` — finalizado y con resultado.
* `Cancelled` — cancelado antes de obtener evidencia suficiente.
* `Inconclusive` — finalizado, pero sin evidencia suficiente para concluir.

---

## Plantilla de experimento

Para experimentos que requieran mayor detalle:

````markdown
# EXP-XXX — Título

**Fecha de inicio:** YYYY-MM-DD
**Fecha de finalización:** YYYY-MM-DD
**Responsable:** Nombre
**Área:** strategy | sales | research | sop | technology | other
**Estado:** Planned | Running | Completed | Cancelled | Inconclusive

## Hipótesis

¿Qué creemos que podría ser cierto?

La hipótesis debe ser concreta y susceptible de ser contrastada.

## Contexto

¿Por qué estamos probando esto?

¿Qué evidencia o situación originó la hipótesis?

## Predicción

¿Qué esperamos observar si la hipótesis es correcta?

## Acción

¿Qué vamos a hacer exactamente?

## Métrica

¿Cómo determinaremos el resultado?

Definir, cuando sea posible:

- métrica principal;
- métrica secundaria;
- periodo;
- población o muestra;
- criterio de éxito.

## Resultado esperado

¿Qué resultado nos llevaría a continuar, modificar o abandonar la hipótesis?

## Resultado observado

¿Qué ocurrió realmente?

Separar los datos observados de las interpretaciones.

## Aprendizaje

¿Qué aprendimos?

## Decisión resultante

¿Qué cambia como consecuencia del experimento?

Si corresponde, referenciar una decisión:

```text
DEC-XXX
````

## Evidencia

Referencias a:

* datos;
* documentos;
* conversaciones;
* métricas;
* capturas;
* resultados comerciales;
* otras fuentes relevantes.

## Limitaciones

¿Qué podría hacer que el resultado no sea generalizable?

## Próximo paso

¿Qué debería ocurrir después?

````

---

## Calidad de los experimentos

Un experimento debe evitar, cuando sea posible:

- cambiar varias variables sin registrarlo;
- definir el éxito después de observar el resultado;
- confundir opinión con evidencia;
- utilizar muestras insuficientes sin reconocer la limitación;
- concluir causalidad a partir de una simple correlación;
- abandonar una hipótesis sin documentar por qué.

No todos los experimentos necesitan rigor científico formal. El nivel de rigor debe ser proporcional al impacto de la decisión que dependa de ellos.

---

## Relación con decisiones

Los experimentos y las decisiones deben poder relacionarse:

```text
EXP-001
   ↓
Resultado
   ↓
DEC-001
````

o:

```text
DEC-002
   ↓
EXP-004
   ↓
Nuevo resultado
   ↓
DEC-005
```

Esto permite reconstruir cómo evolucionó el conocimiento de Orvental.

---

## Preparación para inteligencia artificial

Los registros deben permanecer suficientemente estructurados para que, posteriormente, sistemas de IA puedan:

* recuperar experimentos relacionados;
* comparar resultados históricos;
* identificar patrones;
* encontrar contradicciones;
* relacionar evidencia con decisiones;
* resumir aprendizajes;
* proponer nuevos experimentos.

La IA debe trabajar sobre evidencia registrada, no sustituirla.

---

## Regla fundamental

> Cada experimento debe producir aprendizaje, incluso cuando la hipótesis no se confirme.

Un resultado negativo, inconcluso o inesperado también es conocimiento institucional cuando queda correctamente documentado.
