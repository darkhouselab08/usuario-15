# Plan de trabajo — Propuesta formal de sociedad (INB-009)

> Cómo vamos a construir la propuesta seria para levantar cabañas adicionales bajo esquema de sociedad.
> Esto es el **plan**, no la propuesta. Funciona como spec de INB-009: requiere aprobación de Franco antes de producir el documento final.
> Guardrail activo: **cero cifras inventadas.** Donde no haya dato real, va marcador `[por definir]`.

---

## 1. Objetivo

Producir una **propuesta formal y presentable** para un propietario de tierras, que lo persuada de aportar el terreno mientras nosotros (como constructora + operador de software) aportamos la edificación y la operación. La propuesta debe sostenerse en el activo que ya existe: **una cabaña construida y funcionando** (Refugio del Cielo) + el software de Vertex Pather.

## 2. Entregable final

- Documento principal en Word/PDF (`ops/socios/`), presentable y serio.
- Opcional: versión resumida tipo deck (reutilizar `pitch-inversionista-2026-07.html` como base visual).
- Un anexo de "supuestos y datos" separado, para que las cifras reales vivan aparte y se puedan actualizar.

## 3. Punto de partida (activos que ya tenemos)

- Cabaña piloto construida y operando → **prueba de concepto real**, no promesa.
- Sitio de reservas listo (`frontend/`).
- Pitch de visión ya hecho (`pitch-inversionista-2026-07.html`).
- Modelo de tres capas de Vertex Pather (construcción · hospedaje · software).

Esto cambia la conversación: no pedimos que crean en una idea, mostramos algo que ya funciona.

## 4. Estructura propuesta del documento final

1. **Resumen ejecutivo** — la oportunidad en media página.
2. **Prueba de concepto** — la cabaña que ya existe, con datos reales de operación `[por definir]`.
3. **La oportunidad** — el terreno y su potencial para N unidades más.
4. **El esquema de sociedad** — quién aporta qué (terreno vs. edificación + operación), y opciones de reparto.
5. **Estructura empresarial** — figura legal propuesta para la constructora/sociedad.
6. **Ruta de financiamiento** — cómo se paga la construcción.
7. **Cómo lo sostiene el software** — el diferencial de Vertex Pather (operación con pocos humanos).
8. **Visión de largo plazo** — el complejo como catalizador (modelo Hamptons/Farrell).
9. **Siguiente paso** — qué le pedimos concretamente al propietario.
10. **Anexo** — supuestos, cifras y fuentes.

## 5. Fases del trabajo

| Fase | Qué se hace | Quién | Necesita de Franco |
|------|-------------|-------|--------------------|
| **F1 · Datos base** | Reunir datos reales de la cabaña piloto (costo de construcción, tiempo, ocupación, tarifa) y del terreno | Franco → orquestador | ✅ datos reales |
| **F2 · Investigación** | Investigar figuras legales de sociedad en Colombia (ej. sociedad, cuentas en participación, fiducia inmobiliaria) y opciones de financiamiento (banca, capital privado, socios) | orquestador (`WebSearch`) | — |
| **F3 · Estrategia de persuasión** | Definir el argumento central para el propietario: qué gana él, cómo se reduce su riesgo, por qué nosotros | orquestador + Franco | decisión de enfoque |
| **F4 · Borrador** | Redactar el documento con la estructura de §4, con marcadores donde falten cifras | orquestador (`docx`) | — |
| **F5 · Números** | Llenar el anexo con cifras reales y escenarios (conservador/base) | Franco → orquestador | ✅ datos reales |
| **F6 · Revisión y cierre** | Verificar (checklist de PROTOCOLO §3), pulir, versión final PDF + deck | orquestador + Franco | aprobación final |

## 6. Datos reales que solo Franco puede aportar

Sin estos, el documento se queda en marcadores (guardrail de no inventar):

- Costo real de construir la cabaña piloto y tiempo que tomó.
- Tarifa por noche y ocupación estimada/real.
- Datos del terreno: tamaño, cuántas unidades caben, estado legal, quién es el propietario.
- Cuánto capital propio puede/quiere poner Franco vs. cuánto se financia.
- Qué reparto le parece justo ofrecer al dueño del terreno (rango).

## 7. Decisiones abiertas (para Franco)

1. **Figura de la sociedad:** ¿el propietario entra como socio con participación, como arrendador del terreno, o mediante fiducia? → se investiga en F2, decides tú.
2. **Alcance de la primera propuesta:** ¿una cabaña más como piloto de sociedad, o el complejo completo de una vez? (Recomendación: empezar con 1–3 unidades, no el complejo entero — más creíble y menos riesgo).
3. **Rol del software en el trato:** ¿se cobra aparte, o es parte del aporte de Vertex Pather a la sociedad?

## 8. Riesgos

- **Cifras inventadas** → prohibido. Todo número sale de F1/F5 o queda como `[por definir]`.
- **Sobre-prometer escala** → el pitch ya aclara que la expansión es ilustrativa; mantener esa honestidad.
- **Repo público** → esta propuesta con datos reales NO se sube mientras el repo sea público (ver CONTEXTO §5 y el riesgo de visibilidad abierto).

## 9. Siguiente paso inmediato

Franco aprueba este plan y arrancamos por **F1 (datos base)** — o, si aún no tienes los números a mano, empezamos por **F2 (investigación de figuras legales y financiamiento)**, que no depende de datos tuyos y adelanta camino.

---

## 10. Ruta de financiamiento — borrador estratégico (260717)

Semilla para la fase F2. No es asesoría financiera formal: la estructura real (sociedad, crédito, impuestos) se valida con abogado y contador en Colombia. Cero cifras hasta tener datos reales.

**Principio rector:** desriesgar antes de levantar capital. La cabaña ya construida convierte el financiamiento en un problema de matemáticas, no de fe. Se financia un modelo que factura, no una idea.

Rutas, de menos a más dilutivas:

1. **Terreno como aporte (no compra)** — el dueño entra como socio aportando tierra; nosotros aportamos edificación + operación. Palanca #1 (es INB-009). Elimina la línea de costo más grande. Resolver primero.
2. **Preventa / capital del cliente** — "miembro fundador", estadías largas prepagadas, co-propiedad fraccional. Financia construcción y valida demanda a la vez.
3. **Flujo del piloto reinvertido** — la caja de la cabaña actual paga la siguiente. Cero dilución, prueba replicación.
4. **Deuda bancaria / líneas de construcción** — banca o líneas tipo Bancóldex/Finagro (turismo rural). Regla: construcción con dinero de corto plazo, operación con largo plazo.
5. **Inversionista externo / capital privado** — reservar para escalar de 3 a N unidades, ya con 2 operando. Estructurar por unidad (cada cabaña como su propio vehículo).

**Secuencia para volverlo real:**
1. Convertir el piloto en máquina de datos (3–6 meses: ocupación, tarifa, costos reales).
2. Cerrar la sociedad del terreno.
3. Construir unidad #2 con el capital más barato (flujo + preventa, no inversionistas).
4. Solo entonces levantar para el resto, desde posición de fuerza.

**Carta diferencial:** el software (Vertex Pather) es lo que hace atractiva la unidad económica — menos gente, más margen. Liderar con eso frente a cualquier financiador.

**Foto de referencia (260717):** Franco compartió una imagen del complejo (cabaña terminada + otra en obra en el mismo valle) — activo visual fuerte para el pitch: muestra el proceso, no solo el resultado.

---

*Plan vivo · 260717 · ligado a INB-009 · guardrails: cero cifras inventadas, nada sensible a repo público.*
