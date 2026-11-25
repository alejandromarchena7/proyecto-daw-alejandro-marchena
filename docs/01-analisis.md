# 01 · Análisis y documentación inicial (RA1)

## 1. Sector y empresas (CE 1a, 1b)

El proyecto se enmarca dentro del sector de entretenimiento digital y software como servicio, concretamente en el nicho de plataformas de catalogación, tracking y comunidades de usuarios para contenido audiovisual.

Clasificación de 5 empresas del sector:

- MyAnimeList: Principal referente en el sector. Ofrece la base de datos más extensa del mercado y foros masivos. Su modelo de negocio se basa en la publicidad intensa, suscripciones premium y venta de datos a productoras.
- AniList: Organización descentralizada/independiente. Ofrece un gestor de anime moderno, de código abierto (API GraphQL) con un fuerte enfoque en el diseño UI/UX y la puntuación de usuarios.
- Kitsu: Startup. Enfoque hiper-social, buscando ser una red social. Monetiza mediante suscripciones (Kitsu PRO) para cambiar temas y avatares.
- TV Time: En desuso desde el 15 de julio de 2026. Era una gran corporación, que aunque no era exclusiva de anime, dominó el sector occidental del tracking audiovisual.
- SIMKL: Empresa mediana. Combina seguimiento de anime, series y películas, destaca por su sincronización a utomáticas con plataformas de streaming populares.

```mermaid
graph TD
    CEO[CEO / Dirección General] --> CTO[CTO / Dpto. Técnico]
    CEO --> CMO[CMO / Marketing y Comunidad]
    CEO --> CFO[CFO / Administración]
    
    CTO --> Backend[Desarrollo Backend & APIs]
    CTO --> Frontend[Diseño UI/UX & Frontend]
    CTO --> QA[Sistemas y QA]
    
    CMO --> Moderacion[Moderación de Foros]
    CMO --> Redes[Social Media Management]
    
    CFO --> Legal[Legal y RGPD]
```
- Funciones por departamento:
    - Dpto. Técnico: Mantenimiento de la BBD, consumo de APIs externas, optimización de tiempos de carga y seguridad de la plataforma.
    - Marketing y Comunidad: Adquisición de usuarios, moderación para hacer un uso correcto de los foros, y fidelización.
    - Administración y Legal: Gestión de ingresos por publicidad/suscripciones, control y costes de servidores, cumplimiento de normativas RGPD
## 2. Necesidades y oportunidades (CE 1c, 1d)

1. **Protección estricta contra spoilers**: Los usuarios dejan de leer un foro por miedo a destripes de la trama. Prioridad media.
2. **Fluidez y carga dinámica**: Las bases de datos actuales son pesadas y requieren múltiples recargas de página para marcar un episodio. Prioridad alta.
3. **Alertas pasivas y nativas**: Los usuarios olvidan cuándo se emiten nuevos episodios y quizá no quieran depender del correo electrónico. Prioridad media.

**Oportunidades de negocio:**
El mercado global de la animación japonesa es uno de los de mayor crecimiento en la industria del entretenimiento. En 2023, el mercado global del anime fue valorado en 31.230 millones de dólares, con una proyección de seguir creciendo en los próximos años, según el informe de mercado de Anime realizado por Grand View Research en el año 2024. Esto genera un público cautivo masivo con altas probabilidades de, al menos plantearse una vez, usar una herramienta como un gestor o una wiki para organizar su consumo.

## 3. Tipo de proyecto elegido (CE 1e)

Durante la fase inicial de este proyecto, valoré como idea principal el desarrollar una aplicación web enfocada en el ámbito social. Sin embargo, bajo el criterio de pensar qué esa idea no se sostendría a largo plazo, decidí descartar esa vía y apostar por KarasuSync por dos razones:

1. Acotación del alcance y viabilidad: Los proyectos orientados a problemáticas sociales del mundo real normalmente abarcan muchos colectivos y muchas situaciones, KarasuSync resuelve y se centra solo en un problema cotidiano muy específico.
   
2. Ajustado a mi perfil profesional: Aunque me hubiera gustado hacer algo relacionado con lo social, pienso que esa alternativa se basaba casi exclusivamente en un sistema de permisos y roles en una BBDD. KarasuSync está planteado para hacer uso de un abanico mucho más completo de las competencias del ciclo. 

## 4. Requisitos y restricciones (CE 1f)

| ID | Requisito | Tipo (funcional / no funcional / restricción) | Cómo se verifica |
|---|---|---|---|
| RF-01 | El sistema permite registrar usuarios nuevos, iniciar sesión, cerrar sesión y validar contraseñas. | funcional |Registro de un usuario de prueba, verificación en MYSQL y acceso a ruta protegida mediante sesión PHP. |
| RF-02 | El sistema muestra un catálogo paginado de animes consumiendo datos en formato JSON desde una API externa. | funcional | Comprobación en la herramienta para desarrolladores de la respuesta HTTP 200 y renderizado correcto de las tarjetas en pantalla |
| RF-03 | El usuario autenticado puede crear y gestionar sus listas personales (viendo, pendientes, completados, favoritos, listas propias...) | funcional | Inserción, modificación y borrado de registros en la tabla de listas de MySQL reflejados en el perfil del usuario. |
| RF-04 | El usuario puede registrar el número de episodios vistos, la fecha de visionado y una puntuación del 1-10 para cada anime de su lista. | funcional | Actualización asíncrona en base de datos y persistencia de los valores tras recargar la página |
| RNF-01 | Rendimiento: La carga inicial de la vista principal y las búsquedas dinámicas deben responder en menos de 2 segundos. | no funcional | Medición de tiempo de respuesta usando las Herramientas para Desarrolladores |
| RNF-02 | Seguridad: Todas las consultas a MySQL utilizan sentencias seguras y todo el tráfico se sirve cifrado bajo HTTPS. | no funcional | Revisión de código y verificación de certificado SSL activo |
| RNF-03 | Usabilidad: La interfaz se adapta sin desbordamiento horizontal desde móvil hasta escritorio. Interfaz responsive. | no funcional | Pruebas visuales con el modo dispositivo de las Herramientas para Desarrolladores |
| RNF-04 | Accesibilidad: La aplicación mantiene estructura HTML semántica y contraste suficiente según estándares WCAG | no funcional | Puntuación igual o superior a 90 en el apartado Accesibility de Google Lighthouse |
| REST-01 | Plazo: El Hito 1 se entrega el 26/11/26 y el MVP funcional debe estar desplegado para la entrega final de marzo | restricción | Cumplimiento de las fechas de entrega. |
| REST-02 | Tecnología: Backend en PHP y MySQL, frontend en HTML, CSS y JS | restricción | Inspección del repositorio |
| REST-03 | Privacidad: No se almacenan datos de personas reales: se emplean usuarios ficticios y datos públicos de APIs externas | restricción | Revisión de registros y cumplimientos de las leyes de Protección de Datos |

### Matriz de trazabilidad

*Une cada objetivo con sus requisitos, y estos con lo que los implementa y los comprueba. Se rellena por completo al final del proyecto; en H1 basta con **objetivo y requisito**.*

> **Guía.** Ejemplo ficticio: *OBJ-01 Gestionar citas → RF-02 Crear una cita → CU-03 → `POST /citas` → prueba P-07.* Cada RF y cada RNF de la tabla anterior debe aparecer aquí.

### Matriz de trazabilidad

| Objetivo | Requisito | Caso de uso | Pantalla o endpoint | Prueba o indicador |
|---|---|---|---|---|
| OBJ-01 Gestionar el acceso y perfiles de usuario | RF-01 | | | pendiente |
| OBJ-02 Explorar el catálogo de anime | RF-02 | | | pendiente |
| OBJ-03 Organizar listas y progreso de visionado | RF-03 | | | pendiente |
| OBJ-03 Organizar listas y progreso de visionado | RF-04 | | | pendiente |
| OBJ-04 Ofrecer una interfaz fluida y sin recargas | RF-05 | | | pendiente |
| OBJ-04 Ofrecer una interfaz fluida y sin recargas | RNF-01 | | | pendiente |
| OBJ-05 Garantizar seguridad, usabilidad y accesibilidad | RNF-02 | | | pendiente |
| OBJ-05 Garantizar seguridad, usabilidad y accesibilidad | RNF-03 | | | pendiente |
| OBJ-05 Garantizar seguridad, usabilidad y accesibilidad | RNF-04 | | | pendiente |

## 5. Obligaciones fiscales, laborales y de prevención (CE 1g)

| Obligación | Por qué le toca | Norma | Estado |
|---|---|---|---|
| IVA e IRPF | Presta servicios digitales y obtiene rendimientos de actividad económica | [Ley 37/1992 (IVA)](https://www.boe.es/buscar/act.php?id=BOE-A-1992-28740) y [Ley 35/2006 (IRPF)](https://www.boe.es/buscar/act.php?id=BOE-A-2006-20764) | sin leer |
| Alta en el RETA | Al trabajar por cuenta propia sin empleados, se debe cotizar en el régimen de autónomos | [Ley 20/2007, Estatuto del Trabajo Autónomo](https://www.boe.es/buscar/act.php?id=BOE-A-2007-13409) | sin leer |
| Protección de datos | La aplicación almacena correos, contraseñas y actividad de los usuarios | [LO 3/2018 (LOPDGDD)](https://www.boe.es/buscar/act.php?id=BOE-A-2018-16673) y [RGPD (UE 2016/679)](https://www.boe.es/doue/2016/119/L00001-00088.pdf) | sin leer |


## 6. Ayudas y subvenciones (CE 1h)

| Campo | Contenido |
|---|---|
| Convocatoria y código | Subvenciones para empresas del Principado de Asturias en la modalidad de Cheques de Innovación y Desarrollo Empresarial, ejercicio 2026 (Agencia SEKUENS) · código BDNS 894180 |
| Fuente y fecha de acceso | [Extracto oficial BOPA en SEKUENS/IDEPA (PDF)](https://www.idepa.es/documents/20147/76120/1.9.Extracto_Convocatoria_Cheques_2026.pdf/857faa5b-949b-cf8e-2dae-5046904cff05) y [Ficha de la ayuda en SEKUENS](https://www.idepa.es/detalle-ayuda/-/asset_publisher/EorU9gEBOv3g/content/ayuda-sekuens-ayudas-a-empresas-del-principado-de-asturias-en-el-marco-del-programa-cheques-de-innovacion-y-desarrollo-empresarial) |
| Quién puede pedirla | Microempresas, pymes y autónomos (empresarios individuales) con centro de trabajo y actividad en el Principado de Asturias y al menos una persona trabajadora (incluido el propio autónomo) |
| Qué cubre / excluye | Cubre servicios externos especializados en transformación digital/TIC (desarrollo de apps o canales digitales, cloud, ciberseguridad, automatización), asesoramiento tecnológico y diseño. Excluye la compra de hardware, licencias de software y gastos con entidades vinculadas |
| Cuánto | 50 % del gasto subvencionable (importes fijos desde 1.250 € hasta un máximo de 7.500 €, sobre un presupuesto máximo de 15.000 €) |
| Plazo | Del 26-mar-2026 al 30-abr-2026 |
| Cómo se pide | Vía telemática a través de la sede electrónica de la Agencia SEKUENS |
| Estado | cerrada |

## 7. Guion de trabajo (CE 1i)

| Fase | Fechas | Tareas principales | Responsable | Hito |
|---|---|---|---|---|
| Análisis | 6-nov a 26-nov | Estudio del sector; requisitos | Yo | H1 26-nov |
| Diseño | 26-nov a 10-dic | Viabilidad; modelo de datos | Yo; el tutor revisa | — |
| Planificación | 10-dic a 21-ene | Iniciación en Backend | Yo | H2 21-ene |
| Implementación | 21-ene a 31-mar | Profundización en Backend | Yo; el tutor revisa | — |
| Pruebas | 1-abr a 23-abr | Plan de pruebas; corrección de fallos | Yo | — |
| Despliegue | 26-abr a 7-may | Puesta en marcha; guía de despliegue | Yo | H3 7-may |
| Seguimiento y cierre | 11-feb a 18-jun | Seguimiento; memoria; defensa | Yo; el tutor evalúa | — |

## 8. Glosario

| Término | Definición | Sinónimos que NO uso |
|---|---|---|
| Catálogo | Conjunto de animes consultables en la aplicación obtenidos desde la API externa. | inventario, biblioteca, repertorio |
| Episodio | Cada una de las partes secuenciales que componen un anime. | capítulo, entrega, tomo |
| Lista personal | Agrupación creada por un usuario para clasificar sus animes según su estado (viendo, pendientes, completados, favoritos). | colección, estantería, carpeta |
| Progreso | Registro del número de episodios vistos y la fecha de visionado de un anime dentro de una lista personal. | avance, tracking, marcado |
| Puntuación | Valoración numérica del 1 al 10 que un usuario asigna a un anime. | nota, calificación, rating |
| Spoiler | Revelación de detalles relevantes de la trama de un anime o episodio que otro usuario aún no ha visto. | destripe, filtración, adelanto |

---

## Criterios de evaluación de este documento (RA1, texto literal)

- **1a)** Se han clasificado las empresas del sector por sus características organizativas y el tipo de producto o servicio que ofrecen.
- **1b)** Se han caracterizado las empresas tipo indicando la estructura organizativa y las funciones de cada departamento.
- **1c)** Se han identificado las necesidades más demandadas a las empresas.
- **1d)** Se han valorado las oportunidades de negocio previsibles en el sector.
- **1e)** Se ha identificado el tipo de proyecto requerido para dar respuesta a las demandas previstas.
- **1f)** Se han determinado las características específicas requeridas al proyecto.
- **1g)** Se han determinado las obligaciones fiscales, laborales y de prevención de riesgos y sus condiciones de aplicación.
- **1h)** Se han identificado posibles ayudas o subvenciones para la incorporación de nuevas tecnologías de producción o de servicio que se proponen.
- **1i)** Se ha elaborado el guión de trabajo que se va a seguir para la elaboración del proyecto.
