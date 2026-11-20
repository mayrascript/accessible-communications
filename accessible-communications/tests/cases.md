# Test cases (review mode)

Each case: input → expected findings → ideal output. Run the skill with the input and compare. "No finding" cases guard against false positives.

## Case 1 — Classic bad announcement (expect 7 findings)

**Input**
> 🎉 ¡Call for Speakers abierto! Ven a dar una charla en DevFest Bogotá. Evento 100% inclusivo con intérprete de señas. Más info: llámanos al 300 000 0000. Regístrate: https://ejemplo.org/registro

**Expected findings**
1. Blocker: "100% inclusivo" → replace with specifics.
2. Blocker: voice-only contact → add written channel.
3. Fix: "intérprete de señas" with no named language → LSC (if confirmed) and scope.
4. Fix: registration link, no accommodations field → add optional field.
5. Fix: no alt text/flyer info check → mark pending verification.
6. Suggestion: "Call for Speakers" → "convocatoria de propuestas (CFP)".
7. Suggestion: "charla" → "sesión / presentación" (soft; do not block).
8. Pending verification: whether interpretation is confirmed and which sessions are covered. Do not promise it until confirmed.

**Ideal corrected output**
> 🎉 ¡Convocatoria de propuestas (CFP) abierta para DevFest Bogotá! Envía tu sesión o presentación técnica.
> Ajustes de accesibilidad confirmados: interpretación en Lengua de Señas Colombiana (LSC) en la sala principal y en los talleres. Subtítulos en tiempo real: en confirmación.
> ¿Necesitas algún ajuste para participar? Indícalo en el formulario o escríbenos a accesibilidad@ejemplo.org o por WhatsApp.
> Regístrate: https://ejemplo.org/registro

## Case 2 — Offensive terminology (expect 2 findings)

**Input**
> Contamos con apoyo para asistentes sordomudos y discapacitados auditivos. Habrá un traductor de lenguaje de señas.

**Expected**
- Blocker: "sordomudos" → "personas Sordas" (Deaf people have functional vocal cords).
- Fix: "discapacitados auditivos" → "personas Sordas e hipoacúsicas".
- Fix: "traductor de lenguaje de señas" → "intérprete de Lengua de Señas" + name the language.
- Tone check: no scolding, one-line reason each.

**Ideal**
> Contamos con intérprete de Lengua de Señas Mexicana (LSM) para personas Sordas e hipoacúsicas en las sesiones del auditorio A.

## Case 3 — False positive: audio hardware (expect NO finding on "speaker")

**Input**
> Gracias al equipo de sonido por el speaker nuevo del auditorio. ¡Se escuchó genial!

**Expected:** no terminology finding. "speaker" is hardware. Optional note only if the post claims accessibility.

## Case 4 — False positive: official names and quotes (expect NO finding)

**Input**
> Nos vemos en el "Keynote Speakers Dinner" y en "Tech Talks Bogotá", ambos citados en la agenda oficial.

**Expected:** no rename suggestion; official names kept as given.

## Case 5 — Event with no accessibility mention

**Input**
> Meetup de Kubernetes, sábado 14 a las 3 pm en Medellín. Cupos limitados. Inscripción: https://ejemplo.org

**Expected:** Fix: propose a truthful accessibility line limited to confirmed support + accommodations field. Mention reserved seats with line of sight only if interpretation exists. Do not invent support.

## Case 6 — Interpreter hired from generic staffing agency

**Input**
> Contratamos intérprete a través de la agencia de staffing del venue. Llega el día del evento.

**Expected**
- Fix: require verifiable credentials and technical-event experience.
- Fix: share slides and glossary 48-72 h ahead (impossible if name unknown until the day).
- Suggestion: ask the Deaf attendee or local Deaf organizations for trusted agencies.
- No last-minute substitution without validation.

## Case 7 — Video with captions

**Input**
> Ya está el video completo en YouTube: https://youtu.be/xxxx (subtítulos automáticos activados).

**Expected:** Fix: automatic captions only → human review for names and jargon, high-contrast display. Do not claim the link was opened; mark "pending verification".

## Case 8 — Flyer-only information

**Input**
> [Imagen del flyer con fecha, lugar y QR] Descripción: "¡Nos vemos!"

**Expected:** Blocker: essential info only in image/QR → repeat in text. Fix: draft alt text. Mark alt-text presence on the live post as pending verification.

## Case 9 — Clean post (expect "no issues")

**Input**
> Convocatoria de propuestas abierta hasta el 30 de marzo. Interpretación en LSC en todas las salas (confirmada). Subtítulos humanos en la sala principal. ¿Necesitas algún ajuste? Escríbenos a accesibilidad@ejemplo.org. Registro: https://ejemplo.org

**Expected:** no blockers; at most a suggestion to state the request deadline.

## Case 10 — Self-identification

**Input**
> Soy una persona sorda y prefiero que me digan "sorda".

**Expected:** do not "correct" to "Sorda". Respect the author's own wording.
