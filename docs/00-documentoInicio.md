# 00 · Documento de inicio del proyecto

> **Plantilla.** Se rellena **en la sesión de Inicio (6-nov-2026)** y se afina hasta el **12-nov**, donde el tutor aprueba la propuesta. Es breve: una página. Si algo no lo sabes todavía, escribe «pendiente» y por qué. Borra las notas en cursiva al rellenar.
>
> **No escribas datos personales sensibles** (teléfono, dirección, DNI) ni tu correo personal.

## 1. Datos del alumno/a

| | |
|---|---|
| **Nombre** (real o alias, como prefieras: [por qué](publicacion-y-privacidad.md)) | Alejandro Marchena Moreno |
| **Usuario de GitHub** | alejandromarchena7 |
| **Repositorio del proyecto** | [proyecto-daw-alejandro-marchena](https://github.com/alejandromarchena7/proyecto-daw-alejandro-marchena) |
| **Ciclo y curso** | DAW, 2.º · curso 2026-27 |
| **Fecha** | 2026-11-06 |

## 2. Nombre del proyecto

KarasuSync: Sincroniza tus animes a la velocidad de un cuervo

## 3. Qué quiero hacer

Una aplicación web dónde el usuario podrá catalogar en listas distintos tipos de anime: favoritos, pendientes, los pertenecientes a un mismo estudio..., además, podrán llevar un registro de cuántos episodios se han visto de dicho anime, en qué fecha, comentar y puntúar episodios...

## 4. Qué problema o necesidad resuelve

KarasuSync resuelve un problema: la desorganización. Muchas personas, principalmente personas que no suelen ver muchos animes, no llevan una cuenta de cuántos episodios se han visto de un anime o el número total de animes vistos, normalmente es la plataforma de streaming dónde ven ese contenido la que se encarga de enumerar los capítulos vistos para ofrecer "ver el siguiente", pero, ¿qué pasa si ese anime deja de existir en esa plataforma?, o si dejamos de pagar dicha plataforma. KarasuSync ofrece llevar un orden de los episodios vistos y además ofrecer nuevas recomendaciones una vez hayas terminado un anime.

## 5. Para quién

KarasuSync está pensado para un público general.

## 6. Funcionalidades principales

| # | Funcionalidad | ¿Imprescindible? (sí / no) |
|---|---|---|
| 1 |Registro, autenticación y gestión de perfiles de usuario |Sí |
| 2 |Explorador de catálogo de anime |Sí |
| 3 |Listas personales: marcar episodios como vistos, fechas y puntuar |Sí |
| 4 |Filtrado dinámico en la interfaz sin recargar en la página |Sí |
| 5 |Foros de discusión por episodio con bloqueo de visibilidad anti-spoilers |No ahora |
| 6 |Implementación de notificaciones PUSH para notificar si se ha estrenado un nuevo capítulo |No ahora |

## 7. Tecnologías previstas

| Tecnología | Para qué | Nivel actual (nada / algo / bien) |
|---|---|---|
|PHP y MYSQL |Backend lógico, gestión de BBDD, operaciones CRUD |Bien |
|HTML, CSS y JS|Diseño de la interfaz, peticiones asíncronas y filtrado de elementos en el DOM. |Bien |
|Ubuntu Server, Apache2 y OpenSSL |Entorno de despliegue, configuración de VirtualHosts y securización con certificados SSL |Bien |
|Git / GitHub | Control de versiones, ramas y documentación |Bien |

## 8. Dónde se integra con los módulos de 2.º

- [x] Desarrollo web en entorno cliente (0612)
- [x] Desarrollo web en entorno servidor (0613)
- [x] Despliegue de aplicaciones web (0614)
- [x] Diseño de interfaces web (0615)

## 9. Datos y empresas

- ¿El proyecto parte de una **empresa** (por ejemplo, de tus prácticas)? **No**. Se plantea como un proyecto propio simulando un entorno de producción real.
- ¿Usará **datos personales reales**? **No**. Se generarán datos ficticios si fuera necesario para los usuarios, y se consumirá información pública de APIs públicas.

## 10. Riesgos y dudas iniciales

- Gestionar una API externa: Controlar la API para que la aplicación no se bloquee al cargar grandes búsquedas.
- Gestión del tiempo y alcance: No calcular adecuadamente los tiempos de cada fase, pues en cierta parte tengo la sensación de querer abarcar demasiado con este proyecto.
- Seguridad en el despliegue: La correcta configuración de los certificados de seguridad en el servidor Apache, requisito indispensable para mantener la seguridad de la página.
- Optimización de BBDD: Diseñar de forma eficiente las consultas relacionales en MySQL para que el rendimiento de la aplicación no se ralentice a medida que crezca el número de usuarios y listas de animes registradas.

## 11. Qué espero aprender

Busco consolidar el ciclo mediante este proyecto, integrando múltiples tecnologías, desde el diseño de la interfaz hasta la configuración del servidor. A la vez que aplico principios de integración y experiencia de usuario para construir una plataforma comunitaria accesible, segura y útil

---

## Aprobación del tutor

*Esta parte la rellena el tutor.*

| Criterio mínimo | Cumple |
|---|---|
| Necesidad real y documentada | ☐ |
| Alcance abordable en el tiempo disponible | ☐ |
| Integra contenidos de al menos tres módulos de 2.º | ☐ |
| No usa datos personales reales | ☐ |

**Estado:** ☐ Aprobada · ☐ Aprobada con cambios · ☐ Necesita rehacerse

**Fecha:** 

**Comentarios del tutor:**
