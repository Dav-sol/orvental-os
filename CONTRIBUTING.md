# Contributing to Orvental OS

Este documento define las reglas mínimas para contribuir al repositorio institucional de Orvental.

## 1. Principios

* Mantener el repositorio simple y portable.
* Preferir Markdown y formatos abiertos.
* No duplicar información que ya tenga una fuente de verdad.
* Los cambios importantes deben quedar versionados en Git.
* La complejidad del proceso debe ser proporcional al tamaño del equipo.

## 2. Convención de nombres

### Directorios

Usar:

* minúsculas;
* nombres descriptivos;
* `kebab-case` cuando existan varias palabras.

Ejemplos:

```text
strategy/
sales/
research/
decisions/
go-to-market/
```

### Archivos Markdown

Usar:

```text
kebab-case.md
```

Ejemplos:

```text
vision.md
positioning.md
go-to-market.md
discovery.md
pricing.md
```

Evitar:

```text
Vision.md
GoToMarket.md
documento nuevo.md
final-final.md
```

### Decisiones

Las decisiones permanentes se almacenan en:

```text
decisions/
```

Formato recomendado:

```text
YYYY-MM-DD-short-description.md
```

Ejemplo:

```text
2026-09-30-git-as-source-of-truth.md
```

### Experimentos

Los experimentos se registran en:

```text
research/experiments.md
```

Cada experimento debe tener un identificador estable cuando sea necesario referenciarlo:

```text
EXP-001
EXP-002
EXP-003
```

## 3. Commits

Usar mensajes descriptivos y consistentes.

Formato:

```text
type: description
```

Tipos principales:

```text
feat
fix
docs
refactor
chore
test
```

Ejemplos:

```text
docs: add Orvental vision
docs: define naming conventions
feat: add lead qualification process
fix: correct discovery workflow
chore: update repository structure
```

El mensaje debe describir el cambio realizado, no la intención futura.

## 4. Ramas

Para cambios pequeños y de bajo riesgo puede utilizarse directamente `main` mientras el equipo sea pequeño.

Para cambios importantes o que requieran revisión:

```text
feature/<description>
docs/<description>
fix/<description>
```

Ejemplos:

```text
docs/update-positioning
feature/lead-qualification
fix/experiment-template
```

## 5. Documentación

Antes de crear un nuevo documento:

1. Verificar si la información ya existe.
2. Determinar cuál es su fuente de verdad.
3. Evitar duplicaciones.
4. Mantener cada documento enfocado en un propósito.

Si una herramienta externa contiene información operativa, no copiar automáticamente todo su contenido al repositorio.

El repositorio debe conservar únicamente el conocimiento institucional que deba sobrevivir a la herramienta.

## 6. Cambios importantes

Los cambios de:

* estrategia;
* posicionamiento;
* ICP;
* ofertas;
* metodología;
* procesos;
* decisiones arquitectónicas u operativas;

deben quedar documentados y versionados en Git.

## 7. Revisión

Antes de integrar cambios:

```bash
git diff --check
git status
```

Los cambios deben ser comprensibles y no incluir secretos, credenciales ni información que no corresponda al repositorio.

## 8. Regla general

> Si una regla puede mantenerse simple, no crear una capa adicional de proceso para ella.
