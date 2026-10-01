# Orvental — Infrastructure

## Propósito

Este directorio contiene la infraestructura ejecutable de Orvental en el entorno de desarrollo/autohospedaje.

El objetivo es mantener separadas:

* la documentación institucional;
* el código fuente;
* la infraestructura;
* los datos persistentes;
* los secretos;
* los backups.

La infraestructura debe poder migrarse a otro servidor sin modificar el conocimiento institucional almacenado en Git.

## Estructura

```text
services/
├── plane/       # Infraestructura de Plane
├── twenty/      # Infraestructura de Twenty
├── n8n/         # Infraestructura de n8n
├── config/      # Configuración no secreta
├── backups/     # Referencias/configuración de backups
├── .env.example
├── .gitignore
└── README.md
```

Los datos vivos de los servicios no se almacenan dentro del repositorio.

## Principios

### 1. Los servicios son reemplazables

Plane, Twenty y n8n son herramientas de infraestructura. Orvental OS no debe depender de implementaciones propietarias o específicas de un servidor.

### 2. Los datos sobreviven a los servicios

Los datos persistentes deben almacenarse mediante volúmenes o directorios claramente definidos y separados de la configuración efímera de los contenedores.

### 3. Los secretos nunca entran a Git

Contraseñas, tokens, API keys, credenciales OAuth y otros secretos deben permanecer fuera del repositorio.

Los archivos `.env` reales no deben versionarse.

Los valores necesarios para configurar un servicio deben documentarse mediante `.env.example` sin incluir secretos reales.

### 4. Configuración ≠ secreto

**Configuración versionable:**

* nombres de servicios;
* puertos;
* nombres de redes;
* rutas;
* flags no sensibles;
* versiones de imágenes;
* parámetros operativos no confidenciales.

**Secretos:**

* contraseñas;
* tokens;
* API keys;
* claves privadas;
* credenciales de terceros.

### 5. Portabilidad

La infraestructura debe poder reconstruirse en otro servidor siguiendo documentación versionada.

DaveCloud es el entorno actual, no una dependencia arquitectónica permanente.

## Red

Los servicios internos de Orvental utilizan la red Docker:

```text
orvental
```

Los servicios deben comunicarse internamente mediante esta red cuando corresponda.

El acceso administrativo se realiza mediante la infraestructura privada definida para el entorno.

No se debe exponer directamente Plane, Twenty, n8n, PostgreSQL u otros servicios internos a Internet público sin una decisión explícita y documentada.

## Persistencia

Los datos persistentes de Orvental viven fuera del repositorio:

```text
/workspace/data/orvental/
├── plane/
├── twenty/
├── n8n/
└── postgres/
```

Los backups viven independientemente de los contenedores:

```text
/workspace/backups/orvental/
```

Esta separación permite reconstruir o eliminar contenedores sin perder los datos persistentes y facilita la migración de Orvental a otro servidor.

Los datos persistentes no deben entrar en Git.

Antes de desplegar cada servicio se debe documentar:

* qué datos genera;
* dónde viven;
* qué dependencias tiene;
* cómo se respaldan;
* cómo se restauran.

## Backups

Los backups de Orvental se almacenan en:

```text
/workspace/backups/orvental/
```

La estrategia definitiva debe documentar:

1. qué datos se respaldan;
2. método de backup;
3. ubicación;
4. frecuencia;
5. retención;
6. procedimiento de restauración.

Un backup no se considera confiable hasta haber probado su restauración.

## Operación

Cada servicio debe documentar, cuando corresponda:

* instalación;
* configuración;
* inicio;
* detención;
* actualización;
* logs;
* backup;
* restore;
* eliminación/reconstrucción.

Las operaciones destructivas sobre datos persistentes deben realizarse de forma explícita y documentada.

## Migración

La infraestructura debe poder migrarse desde DaveCloud a otro servidor.

La prueba conceptual es:

> ¿Podemos reconstruir Orvental en otro servidor sin perder el sistema ni sus datos?

La reconstrucción debe depender de:

* Git;
* configuración documentada;
* datos persistentes;
* backups;
* secretos gestionados mediante un mecanismo separado.

No debe depender de conocimiento informal almacenado únicamente en DaveCloud.

## Estado

**v0.1 — Infrastructure Foundation**

Base física preparada:

* red Docker `orvental`;
* estructura de persistencia;
* directorio de backups;
* separación entre repositorio y datos;
* `.env.example`;
* `.gitignore`.

Siguiente etapa: definir y desplegar progresivamente los servicios de infraestructura.
