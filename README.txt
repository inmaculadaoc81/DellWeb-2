INFORMÁTICOSEXPRESS ONE PAGE (rebrand de "DellTech Alienware")

Este repositorio (DellWeb-2) era una copia de la plantilla DellTech
Alienware (informaticosmoncloa.com.es). Por indicación del cliente, se
ha reconvertido por completo en una marca nueva: InformáticosExpress
(informaticosexpress.com), servicio técnico informático multimarca en
Madrid (ya no específico de Dell/Alienware).

CAMBIOS DE MARCA APLICADOS:
- Nombre: DellTech Alienware → InformáticosExpress, en title, meta
  description, og:*, cabecera, footer, formulario, chatbot (título y
  mensaje inicial), schema.org y sección de cita (Cal.com).
- Logotipo: se han creado dos logotipos SVG nuevos (no existía ninguno
  proporcionado por el cliente):
  - assets/logo-informaticosexpress.svg (cabecera y footer)
  - assets/favicon-informaticosexpress.svg (icono del navegador)
  Estilo: icono de "checklist" sobre una insignia azul degradada
  (mismos tonos --blue/--blue2 ya usados en la web) + wordmark en dos
  colores ("Informáticos" en tinta oscura, "Express" en azul de
  acento). Eliminados los archivos antiguos
  assets/logo-delltech.webp y assets/favicon-delltech.webp.
- Contenido generalizado: se ha quitado el enfoque específico en Dell
  y Alienware (textos, kickers y encabezados) y sustituido por
  lenguaje neutro de "ordenador"/"equipo", para que no sea contenido
  duplicado respecto a DellTech. La sección de dos columnas
  "trabajo vs. gaming" se ha mantenido (es un contraste válido para
  cualquier marca), solo se ha quitado la mención a Dell/Alienware.
- Dominio: informaticosexpress.com. Aplicado en canonical, og:url,
  robots.txt, sitemap.xml y JSON-LD.
- Google Analytics: G-2ZWFT3M48L (código nuevo y propio de esta marca;
  no reutiliza el G-3JCBHJ8DCD de DellTech).
- Schema.org: no existía pese a lo que indicaba un README anterior de
  la plantilla original; añadido LocalBusiness completo (nombre,
  teléfono, dirección, areaServed, sameAs).
- Sección SEO: no existía; añadida sección "Guía" (id="guia", enlazada
  en el menú) con contenido propio sobre averías habituales.
- H1 de portada reescrito, corto, directo y totalmente afirmativo (sin
  interrogación ni condicionales), sin forzar ninguna marca (taller
  multimarca): "Tu ordenador no funciona. Aquí lo diagnosticamos sin
  compromiso." Tamaño del H1 aumentado: clamp(38-58px) →
  clamp(46-74px) en escritorio, 40px → 48px en móvil.
- package.json: renombrado a "informaticosexpress-onepage".
- middleware.mjs: ya existía (redirección 301 de URLs antiguas de
  /modelos/, heredado de la conversión a one-page de DellTech); solo
  se ha actualizado el comentario de cabecera con el nuevo nombre.

⚠️ PENDIENTE DE CONFIRMAR (no resuelto, no tocado por falta de datos
nuevos del cliente):
- Teléfono: se ha mantenido +34 910 05 31 43 (el mismo de DellTech),
  ya que no se indicó un número nuevo para InformáticosExpress.
  Confirmar si debe seguir siendo el mismo o si hace falta uno propio.
- Google Maps / Google Business: el enlace y el iframe embebido siguen
  apuntando a la misma ficha física de Madrid, que en Google todavía
  aparece registrada como "DellTech Alienware Servicio Técnico de
  Ordenadores Dell". No se ha creado una ficha nueva de Google
  Business para InformáticosExpress (no es algo que se pueda hacer
  desde el código). Revisar si conviene actualizar esa ficha o crear
  una nueva.
- YouTube: se mantiene el mismo canal compartido de la familia
  Kelatos.

Variables SMTP compartidas (sin cambios):
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada solo en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web; solo se usa en backend.
api/contacto.js ya usaba SMTP + nodemailer; no requería cambios.
