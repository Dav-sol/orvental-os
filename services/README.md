Orvental — Infrastructure

Propósito

Este directorio contiene la infraestructura ejecutable de Orvental en el entorno de desarrollo/autohospedaje.

El objetivo es mantener separadas:

- la documentación institucional;
- el código fuente;
- la infraestructura;
- los datos persistentes;
- los secretos;
- los backups.

La infraestructura debe poder migrarse a otro servidor sin modificar el conocimiento institucional almacenado en Git.

Estructura

/workspace/services/orvental/
├── plane/       # Infraestructura de Plane
├── twenty/      # Infraestructura de Twenty
├── n8n/         # Infraestructura de n8n
├── config/      # Configuración no secreta
├── backups/     # Backups locales/temporales
└── README.md

Principios

1. Los servicios son reemplazables

Plane, Twenty y n8n son herramientas de infraestructura. Orvental OS no debe depender de implementaciones propietarias o específicas de un servidor.

2. Los datos sobreviven a los servicios

Los datos persistentes deben almacenarse mediante volúmenes o directorios claramente definidos y separados de la configuración efímera de los contenedores.

3. Los secretos nunca entran a Git

Contraseñas, tokens, API keys, credenciales OAuth y otros secretos deben permanecer fuera del repositorio.

Los archivos ".env" reales no deben versionarse.

Los valores necesarios para configurar un servicio deben documentarse mediante ".env.example" sin incluir secretos reales.

4. Configuración ≠ secreto

Configuración versionable:

- nombres de servicios;
- puertos;
- nombres de redes;
- rutas;
- flags no sensibles;
- versiones de imágenes;
- parámetros operativos no confidenciales.

Secretos:

- contraseñas;
- tokens;
- API keys;
- claves privadas;
- credenciales de terceros.

5. Portabilidad

La infraestructura debe poder reconstruirse en otro servidor siguiendo documentación versionada.

DaveCloud es el entorno actual, no una dependencia arquitectónica permanente.

Red

Los servicios internos de Orvental deben permanecer en una red privada.

El acceso administrativo se realiza mediante la infraestructura privada definida para el entorno.

No se debe exponer directamente Plane, Twenty, n8n, PostgreSQL u otros servicios internos a Internet público sin una decisión explícita y documentada.

Persistencia

Los datos persistentes deben identificarse explícitamente antes de desplegar cada servicio.

Como mínimo se debe documentar:

- qué datos existen;
- dónde viven;
- cómo se respaldan;
- cómo se restauran;
- qué dependencia tienen de cada servicio.

Backups

Los backups deben ser independientes de los contenedores que generan los datos.

Cada servicio debe documentar:

1. datos que deben respaldarse;
2. método de backup;
3. ubicación del backup;
4. frecuencia;
5. procedimiento de restore.

Un backup no se considera confiable hasta haber probado su restauración.

Operación

Cada servicio debe documentar:

- instalación;
- configuración;
- inicio;
- detención;
- actualización;
- logs;
- backup;
- restore;
- eliminación/reconstrucción.

Migración

La infraestructura debe poder migrarse desde DaveCloud a otro servidor.

La prueba conceptual es:

«¿Podemos destruir DaveCloud y reconstruir Orvental en otro servidor sin perder el sistema ni sus datos?»

La respuesta debe depender de:

- Git;
- configuración documentada;
- backups;
- datos persistentes;
- secretos disponibles por un mecanismo separado.

No debe depender de conocimiento informal almacenado únicamente en DaveCloud.

Estado

v0.1 — Infrastructure Foundation

Actualmente se prepara la estructura para:

- Plane
- Twenty
- n8n

Los servicios se desplegarán progresivamente y solo después de definir su persistencia, configuración y estrategia de recuperación.
