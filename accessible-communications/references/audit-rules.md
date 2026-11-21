# Audit Rules (review mode)

Use when the user asks to review, audit, or "check" an announcement, CFP, registration page, social post, or schedule. These rules are semantic: judge intent in context, never match keywords blindly.

## Report format

Return findings grouped by severity. Each finding: **quote** → **why it matters (one sentence)** → **suggested rewrite**. End with "Pending verification" (checks you could not perform: image alt text actually present, captions actually reviewed, links opened).

- **Blocker:** misleads attendees or excludes (vague interpretation claim, unconfirmed support promised, voice-only contact, offensive term).
- **Fix:** missing standard element (accommodation field, named sign language, alt text).
- **Suggestion:** style or terminology preference. Offer, never insist.

Tone: colleague, not censor. Assume good faith; most errors are common habits. Explain the "why" briefly. Never lecture, never shame the author. If nothing is wrong, say so.

## Terminology (flag only when it refers to people, language, or event roles)

| Seen | Suggest | Why (one line) | Severity |
|---|---|---|---|
| "sordomudo", "mudo" | persona Sorda | Obsolete and inaccurate; Deaf people have functional vocal cords. | Blocker |
| "discapacitado auditivo", "sufre de sordera", "no oyente", "deficiente auditivo", "sordito" | persona Sorda / persona hipoacúsica (per the person's own preference) | Defines people by deficit or is condescending. | Fix |
| "lenguaje de señas" | Lengua de Señas | It is a full language, not a general communication ability. | Fix |
| "traductor de señas" (live event) | intérprete de Lengua de Señas | Interpreting is real-time; translation works on written text. | Fix |
| "personas normales" vs. Deaf people | personas oyentes | "Normal" implies others are abnormal. | Fix |
| "capacidades diferentes", "especiales", "minusválido" | persona con discapacidad | Euphemism or demeaning. | Fix |
| "speaker" referring to a presenter | ponente / expositor/a / conferencista | Speaking is not the only way to present; plain Spanish. | Suggestion |
| "charla", "talk" referring to a session | sesión / presentación / ponencia | Not limited to chatting aloud. | Suggestion (colloquial "charla" is common; never block) |
| "Call for Speakers" | convocatoria de propuestas (CFP) | Values the proposal, not oral delivery. | Suggestion |

Capital "Sorda" refers to cultural identity; lowercase "sordo" to the audiological condition. Respect the person's own self-identification when known; apply the table only to the author's wording about others.

### Do not flag (false-positive guard)

- Audio hardware or sound: "el speaker del salón", "speakers de la sala", "bocinas", "agradecimiento al speaker de audio".
- Official names, brand names, session titles, quotations, and handles (keep as given): "Keynote Speakers Dinner", "Tech Talks Bogotá".
- Code, URLs, hashtags, and file names.
- The same word used by a Deaf person describing themselves.
- A term inside a "what not to say" list written to educate.
- "Talk" in an English-language post written for an English audience.

When unsure whether a term refers to a person, ask instead of flagging.

## Interpreter claims

- Mention of "intérprete", "interpretación en señas", "accesible con señas" without a named language → **Fix:** name the sign language (LSC, LSM, LSA, LSCh, LSP, LSE, ASL, or International Sign for global events). Sign languages are national, not universal. Do not infer the language from the event's country if the audience may be international.
- Interpretation advertised without scope (which sessions, rooms, workshops, networking) → **Fix.** Coverage should not stop at the main stage.
- Interpretation advertised but not confirmed in the brief → **Blocker:** do not present pending support as available.
- Volunteer, bilingual attendee, or AI avatar presented as the interpreter → **Blocker:** professional interpreters are required for technical content.
- Hiring through a generic staffing or events agency → **Fix:** require verifiable credentials (certification, technical-event experience), no last-minute substitutions without validation, and ask the Deaf attendee or local Deaf organizations for trusted providers.

## Accessibility presence

- No mention of accessibility at all in an event announcement → **Fix:** propose a short, truthful line covering only confirmed support, plus the accommodations contact.
- "100 % inclusivo", "totalmente accesible" → **Blocker:** replace with specifics.

## Registration and contact

- Registration link or form with no accommodations field → **Fix:** add an optional "¿Requiere algún ajuste razonable de accesibilidad?" field with options (Intérprete de Lengua de Señas, subtítulos en tiempo real, otro). No diagnosis or certificate. Share answers only with the coordinators.
- Only contact is phone or voice note → **Blocker:** add a written channel (email, WhatsApp, form).
- Deadline for requesting accommodations absent → **Suggestion:** state a realistic lead time.

## Venue and sightlines (event announcements and logistics plans)

- If reserved seating is mentioned: it must give a simultaneous line of sight to speaker, screen, and interpreter, not just "front row".
- If missing and the event offers interpretation: **Suggestion** to mention reserved seats.
- Do not claim sightlines or lighting were verified; mark "pending verification at rehearsal".

## Images, flyers, and video

- Flyer or graphic whose essential info (date, place, link, accommodations) exists only in the image → **Blocker:** repeat it in the post text.
- Image without alt text where the platform supports it → **Fix:** draft concise alt text. Say you could not verify alt text on the live post.
- Video, stream, or recording link → check that captions are stated or confirmed. Captions must be human-reviewed (names, jargon) and high contrast. If captions are only automatic, mark **Fix**. Do not claim you opened the link.
- Color-only status, low-contrast text on image → **Fix.**
- Voice notes or call-only instructions → **Blocker** (text equivalent).

## Out of scope for the audit

Do not send, publish, or edit live pages. Do not judge legal compliance. Do not infer anyone's identity or preferences.
