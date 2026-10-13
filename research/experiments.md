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

## Registro

| ID | Fecha | Hipótesis | Acción | Métrica | Resultado | Aprendizaje | Decisión | Estado |
|---|---|---|---|---|---|---|---|---|
| EXP-001 | YYYY-MM-DD | ... | ... | ... | ... | ... | ... | Planned |
| EXP-002 | 2026-10-13 | Un diagnóstico trazable y una intervención priorizada en Caiman SC permitirán evaluar la utilidad y repetibilidad del Growth Audit; no validan por sí solos la disposición de pago de clientes externos. | Preparar piloto; después discovery, diagnóstico, línea base e intervención autorizada. | Trazabilidad del diagnóstico, disponibilidad de línea base, métrica elegida antes de intervenir, horas/costos. | Pendiente | Pendiente | Pendiente | Planned |

## EXP-002 — Piloto interno Caiman SC: validar el método Growth Audit

**Inicio:** 2026-10-13 (preparación documental; inicio operativo pendiente)  
**Finalización:** Pendiente  
**Responsable:** David Solano  
**Área:** research | sales  
**Estado:** Planned  
**Alcance:** `research/pilots/caiman-sc/README.md`  
**Decisión:** `DEC-001`

### Hipótesis

Un proceso documentado de investigación, diagnóstico, priorización, intervención y medición permitirá evaluar y mejorar el método Growth Audit en un negocio real. La disposición de pago debe validarse después con clientes externos.

### Predicción

Antes de intervenir se documentarán el recorrido comercial, fuentes y límites de evidencia, brechas prioritarias, métricas disponibles y una intervención con aprobación, responsable y criterios de evaluación. Después se registrarán resultados, incluidos los nulos o inconclusos.

### Acción

1. Confirmar alcance y permisos operativos.
2. Realizar discovery.
3. Auditar presencia y proceso comercial.
4. Construir una línea base viable.
5. Elegir prioridades y definir métricas antes del cambio.
6. Ejecutar solo intervenciones autorizadas.
7. Evaluar resultados y actualizar la metodología.

### Métricas

- **Proceso:** trazabilidad y completitud del diagnóstico.
- **Comercial:** se seleccionará tras discovery y antes de intervenir, según disponibilidad y fiabilidad.
- **Secundarias:** origen de consultas, tiempo de respuesta, reservas, visitas, conversión, seguimiento, horas y costos.

No fijar metas numéricas antes de conocer la línea base. Seguidores, impresiones y clics no sustituyen resultados comerciales.

### Resultado esperado

Diagnóstico reproducible, línea base o explicación de por qué no puede construirse, intervención evaluable y aprendizajes para la metodología. No se presupone aumento de ingresos.

### Resultado observado, aprendizaje y decisión

Pendientes. No se ha iniciado el trabajo operativo ni registrado una intervención.

### Evidencia

- `research/pilots/caiman-sc/README.md`
- `strategy/positioning.md` y `strategy/offers.md`
- `Dav-sol/el-nuevo-caiman-growth-vault`, especialmente `02-research/digital-presence-audit.md` y `02-research/source-registry.md`

### Limitaciones

Relación familiar, posible ausencia de pago, calidad y volumen de datos desconocidos, estacionalidad y factores externos. No inferir causalidad sin evidencia suficiente.

### Próximo paso

Acordar permisos y alcance; iniciar discovery. No modificar perfiles, invertir en publicidad ni publicar el caso sin autorización explícita.

## Estados

- `Planned` — definido, aún no ejecutado.
- `Running` — en ejecución.
- `Completed` — finalizado y con resultado.
- `Cancelled` — cancelado antes de obtener evidencia suficiente.
- `Inconclusive` — finalizado sin evidencia suficiente para concluir.

## Plantilla de experimento

Para experimentos que requieran mayor detalle, registrar:

- Identificador, fechas, responsable, área y estado.
- Hipótesis, contexto, predicción y acción.
- Métrica principal/secundaria, periodo, población y criterio de éxito.
- Resultado observado, aprendizaje y decisión.
- Evidencia y limitaciones.
- Próximo paso.

## Calidad de los experimentos

Evitar cambiar varias variables sin registrarlo, definir el éxito después de observar resultados, confundir opinión con evidencia, ignorar muestras insuficientes o concluir causalidad a partir de correlación. El rigor debe ser proporcional al impacto de la decisión.

## Relación con decisiones

```text
Hipótesis → Experimento → Evidencia → Decisión → Implementación → Resultado
```

Los experimentos y decisiones deben referenciarse entre sí cuando sea útil.

## Preparación para inteligencia artificial

Los registros deben permitir recuperar experimentos, comparar resultados, identificar contradicciones y relacionar evidencia con decisiones. La IA ayuda a analizar la evidencia, pero no la sustituye.

> Cada experimento debe producir aprendizaje, incluso cuando la hipótesis no se confirme.
