# Proyecto Copy + SEO + AEO: misterpressurewash.com

Este directorio es el orquestador del proyecto de copywriting, SEO y AEO de la web de
Mister Pressure Wash, LLC (MPW). Todo el trabajo de texto para la web pasa por aquí.

## Objetivo

Que la web haga tres cosas a la vez, sin sacrificar ninguna:

1. **Vender** (copy): que el visitante correcto pida un estimado.
2. **Posicionar** (SEO): que Google la muestre para "pressure washing [ciudad]" y similares.
3. **Ser citada** (AEO, Answer Engine Optimization): que Google AI Overviews, ChatGPT,
   Perplexity, Gemini y Claude nombren a MPW cuando alguien pregunta por el servicio.

Y una cuarta, transversal: **mejorar cómo escribimos** en todo MPW (web, posts, emails).

## Fuentes de verdad (leer antes de escribir)

Orden de lectura obligatorio para cualquier agente o sesión:

1. `01-metodo-bravo-usa.md`: la metodología de copy (Isra Bravo adaptado a mercado USA).
2. `03-guia-de-estilo.md`: voz de MPW, palabras prohibidas, checklist final.
3. `02-seo-aeo-local.md`: reglas técnicas para que el texto rankee y sea citado.
4. `04-plan-de-paginas.md`: qué páginas existen o faltan, a quién le habla cada una y
   qué búsqueda ataca.

Las reglas de voz vienen del skill `mpw-marketing-copy` (Cowork). Si ese skill cambia,
actualizar `03-guia-de-estilo.md` en el mismo momento. Una sola fuente de verdad por regla.

## Flujo de trabajo por página

1. **Brief**: completar la ficha de la página en `04-plan-de-paginas.md` (audiencia única,
   keyword principal, pregunta que responde, prueba disponible).
2. **Borrador**: subagente `copywriter` (Sonnet). Usa `plantillas/pagina-servicio.md`.
3. **Auditoría SEO/AEO**: subagente `seo-aeo-auditor`. Devuelve lista de fallos concretos.
4. **Edición crítica**: subagente `editor-critico`. Pasa el checklist de Bravo y de estilo.
5. **Alvaro aprueba**. Nada se publica en la web sin aprobación explícita en el chat.

Los subagentes viven en `/.claude/agents/` en la raíz del repo.

## Reglas duras

- Nunca inventar datos: precios, años en el negocio, número de reseñas, garantías,
  certificaciones, ciudades servidas. Si falta un dato, escribir
  `[NEEDS CONFIRMATION: qué falta]` y seguir.
- Nunca publicar. Este proyecto produce borradores en archivos; la publicación en la web
  la hace Alvaro o se autoriza caso por caso.
- Copy final en inglés (mercado USA). Documentación interna en español.
- Cero rayas largas (em dashes) en cualquier texto de cara al cliente.
- Una audiencia por página. Nunca mezclar homeowners con property managers.

## Punto ciego conocido

Este repo (`mpw-finance-bridge-policies`) es la página pública de políticas del Finance
Bridge de QuickBooks. Si GitHub Pages publica la rama `main`, cualquier archivo de este
directorio quedaría público al hacer merge. Recomendación: mover `copywriting/` a un repo
propio (ej. `mpw-website-copy`) antes de hacer merge a `main`.
