# Plantilla: página de servicio

Esqueleto para cualquier página de servicio o de servicio + ciudad. El `copywriter` la
rellena; las secciones marcadas (AEO) son obligatorias para ser citable.

---

**Title tag** (50 a 60 car.): `[Service] in [City], [ST] | Mister Pressure Wash`

**Meta description** (140 a 155 car.): [dibujo del problema]. [resultado]. [acción].

**URL**: `/[service]-[city]-[st]/`

---

## H1: [Service] in [City], [ST]

**Primera frase (AEO + Bravo)**: responde la búsqueda y dibuja el problema en la misma
línea. Ej. estructural (no copiar): "[Visible problem 1], [visible problem 2] and
[visible problem 3]. Mister Pressure Wash [does what] for [audience] in [City] so [outcome]."

**Segunda frase**: la fricción que eliminas.

**Botón**: Get a free estimate

## H2: What you get

3 o 4 resultados, cada uno con su prueba. No lista de tareas; lista de resultados.

## H2: Before and after

2 o 3 fotos reales del mismo ángulo, con alt descriptivo y una línea de historia cada una
(cliente tipo, problema, resultado). Sin nombres sin permiso.

## H2: How it works

3 pasos. El último es siempre qué recibe el cliente (ej. fotos antes/después, reporte).

## H2: What customers say

2 o 3 reseñas reales (texto literal, nombre con permiso, fuente).

## H2: Areas we serve

Lista de ciudades/condados reales con enlace a sus páginas.

## H2: FAQ (AEO)

5 a 8 preguntas reales. Cada respuesta: 40 a 60 palabras, autocontenida, la primera
frase ya responde. Última frase empuja a la acción cuando encaja.

## Cierre

Una línea que vuelve al dibujo del problema + botón. Nada más.

---

## JSON-LD (rellenar, validar en https://validator.schema.org)

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "LocalBusiness",
      "@id": "https://misterpressurewash.com/#business",
      "name": "Mister Pressure Wash, LLC",
      "url": "https://misterpressurewash.com/",
      "telephone": "[NEEDS CONFIRMATION]",
      "address": {
        "@type": "PostalAddress",
        "addressLocality": "Saint Johns",
        "addressRegion": "FL",
        "postalCode": "[NEEDS CONFIRMATION]",
        "addressCountry": "US"
      },
      "areaServed": ["[NEEDS CONFIRMATION: cities/counties]"],
      "sameAs": ["[NEEDS CONFIRMATION: Google, Yelp, Facebook, BBB URLs]"]
    },
    {
      "@type": "Service",
      "serviceType": "[Service]",
      "provider": { "@id": "https://misterpressurewash.com/#business" },
      "areaServed": "[City], [ST]"
    },
    {
      "@type": "FAQPage",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "[Question]",
          "acceptedAnswer": { "@type": "Answer", "text": "[Answer]" }
        }
      ]
    }
  ]
}
```
