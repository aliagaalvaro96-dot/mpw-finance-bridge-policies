# SEO + AEO local para MPW

Glosario rápido:
- **SEO**: aparecer en los resultados normales de Google y en el Map Pack.
- **AEO** (Answer Engine Optimization; también lo llaman GEO): que las IAs (Google AI
  Overviews, ChatGPT, Perplexity, Gemini, Claude) citen o recomienden a MPW cuando alguien
  pregunta. Probablemente es el "AMO" que tenías en mente.

AEO no reemplaza al SEO local, se construye encima. Google AI Overviews cita casi siempre
páginas que ya están en el top 10. Primero SEO, luego estructura "citable".

---

## 1. Lo que más mueve la aguja en negocio local (en orden)

1. **Google Business Profile completo y activo**: categoría principal correcta, todas las
   categorías secundarias válidas, área de servicio, fotos reales cada semana, posts,
   respuestas a todas las reseñas.
2. **Reseñas reales y constantes**: pedir reseña después de cada trabajo terminado
   (automatizable desde Jobber). Las IAs leen el texto de las reseñas: que mencionen
   servicio y ciudad ayuda.
3. **NAP idéntico en todas partes**: mismo nombre, dirección y teléfono en web, Google,
   Yelp, BBB, Facebook, Nextdoor, Angi, directorios de la cámara de comercio y BNI.
4. **Una página por servicio** y **una página por ciudad clave** con contenido real
   distinto (no la misma página cambiando el nombre de la ciudad).
5. **Datos estructurados (schema)** en cada página.
6. **Velocidad y móvil**: la mayoría de búsquedas locales vienen del teléfono.

---

## 2. Reglas de escritura para SEO + AEO

1. **Responder primero, explicar después.** La respuesta a la pregunta de búsqueda va en
   las 2 o 3 primeras frases de la página o sección. La mayoría de citas de AI Overviews
   salen del primer tercio de la página.
2. **Un H1 por página** con servicio + ciudad: "Commercial Pressure Washing in Jacksonville, FL".
3. **H2 como preguntas reales** que la gente escribe: "How often should a restaurant
   drive-thru be pressure washed?" Debajo, respuesta de 40 a 60 palabras autocontenida.
4. **Frases "extraíbles"**: sujeto + verbo + objeto claro. "Mister Pressure Wash cleans
   breezeways and stairwells for apartment communities in Northeast Florida." Una IA
   puede copiar esa frase tal cual.
5. **Entidades explícitas**: nombre completo de la empresa, ciudades, condados, tipos de
   superficie, normas (NFPA 96 si aplica). No "our area", sino "St. Johns, Duval and Clay counties".
6. **FAQ al final de cada página de servicio** (5 a 8 preguntas) con schema FAQPage.
7. **Fecha de actualización visible** en páginas de guía. La frescura cuenta para las IAs.
8. **Nada de texto clave dentro de imágenes o sliders.** Tiene que estar en HTML.
9. **Enlaces internos**: cada página de ciudad enlaza a sus servicios y viceversa.

Esto no choca con Bravo: Bravo dice "lo importante en las dos primeras líneas" y AEO dice
lo mismo. Donde sí hay tensión (las FAQ son más "informativas" que "vendedoras"), la FAQ
responde seca y la última frase de cada respuesta lleva a la acción.

---

## 3. Metadatos por página

- **Title tag**: 50 a 60 caracteres. `Servicio en Ciudad, ST | Mister Pressure Wash`.
- **Meta description**: 140 a 155 caracteres. Dibujo del problema + resultado + acción.
  No afecta al ranking directo, sí al clic.
- **URL**: corta, en minúsculas, con guiones. `/commercial-pressure-washing-jacksonville-fl/`.
- **Alt de imágenes**: descripción real. "Apartment breezeway before and after pressure
  washing in Jacksonville FL".

---

## 4. Schema mínimo

- `LocalBusiness` (subtipo más cercano disponible) en todo el sitio: nombre, teléfono,
  URL, `areaServed`, `sameAs` (Google, Yelp, Facebook, BBB), horario.
- `Service` en cada página de servicio.
- `FAQPage` en cada bloque de FAQ.
- `Review`/`AggregateRating` solo con reseñas propias verificables y siguiendo las
  políticas de Google (no marcar reseñas de terceros como propias).

Plantilla JSON-LD en `plantillas/pagina-servicio.md`.

---

## 5. Medición (qué mirar cada mes)

- Google Search Console: impresiones y clics por página y por consulta.
- Google Business Profile: llamadas, solicitudes de ruta, clics a la web.
- Prueba manual AEO: preguntar a ChatGPT, Perplexity, Gemini y Google (AI Mode) las 10
  preguntas objetivo ("best commercial pressure washing company in Jacksonville" etc.) y
  anotar si MPW aparece. Candidato a automatizar con una Routine mensual.
- Formularios de estimado recibidos desde la web (la métrica que paga las cuentas).
