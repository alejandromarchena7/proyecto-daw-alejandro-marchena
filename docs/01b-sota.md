# 01b · Estado del arte (SOTA) de mi proyecto

> **Plantilla.** En **H1 (26-nov-2026)** entregas una **versión breve** (2-3 páginas: apartados **1, 2 y 5**), junto al `01-analisis.md`. Los apartados 3, 4, 6, 7 y 8 se completan en **H2 (21-ene-2027)** hasta las **4-6 páginas** del documento final. Aquí estudias qué soluciones, **modelos de negocio** y **herramientas** existen ya para el problema que has elegido, y justificas tus decisiones con ello. Cada apartado indica el criterio de evaluación (CE) que alimenta. Borra los bloques «Guía» al rellenar.

> **Guía.** Calendario de H1: **hasta el 18-nov** preguntas de búsqueda y tabla de soluciones (apartados 1 y 2) · **hasta el 25-nov** hueco y diferenciación (apartado 5). Los apartados 3, 4, 6, 7 y 8 son de H2.
>
> **Reglas.**
>
> - Solo cuenta lo que tiene **enlace y fecha de acceso**.
> - Si usas IA para buscar, **abre cada fuente** y comprueba que existe y dice lo que te cuenta la IA. Puede inventar productos, precios o referencias. Decláralo en [`declaracion-uso-ia.md`](declaracion-uso-ia.md).
> - Usa **solo información pública** de las soluciones que estudias. **Nada** de la empresa de prácticas ni de clientes reales.
> - Compara herramientas con **los mismos criterios**, no por opinión. Salvo razón argumentada, prefiere lo que has visto en el ciclo (Java 21, Spring Boot, SQL).
> - Si algo no lo has podido comprobar, dilo en el apartado 8.

## 1. Problema y preguntas de búsqueda (CE 1c)

*El problema en **una frase**. Después, **3-5 preguntas** que vas a contestar con este documento (por ejemplo: «¿Qué soluciones existen?», «¿Cómo ganan dinero?», «¿Qué tecnologías usan?»). Indica **dónde y cuándo** buscaste (buscadores, tiendas de aplicaciones, repositorios, informes del sector).*

**Problema:** Los aficionados al anime tienen dificultades para llevar al día su progreso en múltiples series de forma fluida, sin sufrir sobrecarga publicitaria ni exponerse a spoilers en comunidades masivas.

| # | Pregunta | Dónde busqué | Fecha |
|---|---|---|---|
| P1 | ¿Qué plataformas y herramientas existen actualmente para el seguimiento de anime? | Google, Reddit (r/anime), GitHub | 25-nov-2026 |
| P2 | ¿Qué modelos de negocio y precios utilizan las principales plataformas del sector? | Webs oficiales (MyAnimeList, AniList, Kitsu, SIMKL, TV Time) | 25-nov-2026 |
| P3 | ¿Cuáles son las principales quejas de los usuarios respecto a usabilidad y spoilers? | Foros de Reddit, reseñas en Google Play / App Store | 25-nov-2026 |
| P4 | ¿Existen alternativas de código abierto o APIs públicas gratuitas para obtener el catálogo de anime? | GitHub, documentación oficial de Jikan API y AniList API | 25-nov-2026 |

## 2. Soluciones existentes (CE 1a, 1c, 2a)

*Tabla de **5-8** soluciones (productos, servicios o proyectos de código abierto) que resuelven total o parcialmente el problema. Incluye alguna **alternativa gratuita o de código abierto** y alguna **no digital** (hoja de cálculo, papel) si existe.*

| Solución | Para quién | Qué hace | Modelo de precio | Enlace y fecha de acceso | Estado (`leído` / `sin leer`) |
|---|---|---|---|---|---|
| MyAnimeList | Público general | Mezcla red social, foro y BBDD de anime y manga. El sistema web está basado en listas para organizar y puntuar anime y manga. | El uso de la plataforma es gratuito con anuncios. Ofrece una suscripción opcional llamada MAL Supporter. Además, MAL monetiza mediante la venta digital de mangas en su tienda y acuerdos de afiliación con plataformas de streaming como Tokyo Otaku Mode | [MyAnimeList](https://myanimelist.net) 25-nov-26 | leído  |
| AniList | Público general | Plataforma en línea y red social para catalogar, seguir, puntuar y compartir series y películas de anime, manga, manhwa... También permite organizar títulos vistos, pendientes, en progreso o abandonados. | Completamente gratuito. No cuenta con pagos dentro de su plataforma web. | [AniList](https://anilist.co) 25-nov-26| leído |
| Kitsu | Público general | Seguimiento de anime/manga con feed de actividad, grupos de discusión, reacciones y recomendaciones. | El uso de la plataforma es gratuito. Ofrece una suscripción opcional: Kitsu PRO para personalización y apoyo al proyecto. | [kitsu.app](https://kitsu.app/) 25-nov-26 | leído |
| Ryot | Usuarios técnicos o preocupados por la privacidad que prefieren autoalojar sus propios datos. | Gestor de código abierto todo en uno para hacer seguimiento de anime, series, películas, libros y videojuegos sin publicidad. | Código abierto gratuito. Ofrece versión Pro de pago opcional con funciones avanzadas y sincronización en nube. | [github.com/IgnisDa/ryot](https://github.com/IgnisDa/ryot) 25-nov-2026 | leído |
| "Notas" del móvil/Excel/Hoja de papel | Público en general | Apuntar los episodios vistos por métodos tradicionales y ambiguos. | Gratuito |  |  |

## 3. Modelos de negocio (CE 1d, 1e)

*Qué **patrones** se repiten en las soluciones del apartado 2 (suscripción, *freemium*, comisión por operación, licencia, publicidad, servicio gratuito o público) y por qué. Describe con un **Business Model Canvas** (opcional; el profesor te da el material) **2-3 casos**. Termina con el modelo que seguiría **tu** proyecto, o qué ahorra o mejora si no es un negocio.*

| Patrón | Soluciones que lo usan | Ventaja | Riesgo |
|---|---|---|---|
| [RELLENAR] | | | |

## 4. Herramientas y tecnologías (CE 2a, 2b)

*Para cada decisión técnica importante (lenguaje y *framework*, base de datos, despliegue, autenticación…), compara **2-3 opciones con los mismos criterios**. Marca la que eliges.*

| Decisión | Opción | Madurez | Licencia | Coste | Curva de aprendizaje | Encaje con el ciclo | Elegida |
|---|---|---|---|---|---|---|---|
| [RELLENAR: p. ej. base de datos] | | | | | | | |

*Cada decisión importante se convierte en una decisión registrada en [`decisiones/`](decisiones/0000-plantilla.md).*

## 5. Hueco y diferenciación (CE 1e)

- Frente a webs muy recargadas de publicidad y con navegación pesada (como MyAnimeList), o con mayor influencia sobre series/películas (como TV Time), KarasuSync apuesta por una interfaz limpia, filtrado instantáneo y foros con control de spoilers.
- Plataformas alternativas como MyAnimeList ofrecen prestaciones muy superiores en cuanto al alojamiento y la gestión de reseñas. Además, cuentan con una trayectoria de aproximadamente 20 años en el sector, lo que les ha permitido consolidar una comunidad de millones de usuarios y establecer una base de usuarios fiel y activa.

## 6. Decisiones derivadas (CE 1e, 1f, 2b)

*Qué consecuencias tiene este estudio en tu proyecto.*

- **Tipo de proyecto elegido** (enlaza con el apartado 3 de [`01-analisis.md`](01-analisis.md)): [RELLENAR]
- **Requisitos que salen del estudio** (con su ID del apartado 4 de `01-analisis.md`): [RELLENAR]
- **Decisiones técnicas** (enlace a cada archivo de `decisiones/`): [RELLENAR]

## 7. Fuentes y calidad (CE 2a)

*Al menos **2 fuentes independientes** (no dos páginas de la misma empresa). Datos oficiales o primarios antes que blogs.*

| # | Fuente (enlace) | Tipo | Fecha de acceso | Fiabilidad (alta / media / baja) y por qué |
|---|---|---|---|---|
| F1 | [RELLENAR] | | | |

## 8. Límites

*Qué **no pudiste comprobar** y qué datos son estimaciones. Una lista corta y honesta es mejor que fingir certeza.*

- [RELLENAR]

---

## Criterios de evaluación que alimenta este documento (texto literal)

- **1a)** Se han clasificado las empresas del sector por sus características organizativas y el tipo de producto o servicio que ofrecen.
- **1c)** Se han identificado las necesidades más demandadas a las empresas.
- **1d)** Se han valorado las oportunidades de negocio previsibles en el sector.
- **1e)** Se ha identificado el tipo de proyecto requerido para dar respuesta a las demandas previstas.
- **1f)** Se han determinado las características específicas requeridas al proyecto.
- **2a)** Se ha recopilado información relativa a los aspectos que van a ser tratados en el proyecto.
- **2b)** Se ha realizado el estudio de viabilidad técnica del mismo.

> El SOTA **no añade criterios de evaluación**: reúne en un solo sitio lo que 1a-1f y 2a-2b ya piden. La evaluación sigue las listas de cotejo de H1 y H2.
