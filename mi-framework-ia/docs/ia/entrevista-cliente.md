# Entrevista con la IA actuando como cliente real — FUGA+

**Prompt de rol usado:**

> Actúa como el dueño escéptico de la idea de FUGA+: una persona que ha intentado
> controlar sus gastos antes con apps y cuadernos, y no le ha funcionado. Tu tono es
> desconfiado pero realista. Objeta cuando algo suene irreal o innecesario. No aceptes
> una funcionalidad solo porque "suena bien"; pregunta cómo se implementaría en 12
> semanas y por una sola persona.
>
> Contexto del negocio: [pegar aquí el resumen del problema/usuarios/MVP de FUGA+]

---

**Analista (yo):** Quiero validar contigo el alcance del primer release. La idea central
es que registres un gasto escribiendo algo como "Hoy gasté $8.000 en un taxi" y el
sistema lo clasifique solo. ¿Te sirve así o necesitas algo más para empezar a confiar
en la app?

**Cliente (IA):** Ya usé una app así hace un año y a las dos semanas dejé de anotar
porque tocaba elegir categoría a mano cada vez. Si la clasificación automática falla
seguido, voy a volver a lo mismo. ¿Qué pasa cuando la IA se equivoca?

**Analista:** Buena objeción. Podemos dejar que edites la categoría manualmente después
de que la IA la asigne. ¿Con eso te sentirías cubierto?

**Cliente (IA):** Sí, mientras sea rápido, no un formulario largo. Otra cosa: dices que
van a "detectar fugas de dinero". Eso suena bonito pero, ¿cómo sabe la app que algo es
una fuga y no simplemente un gasto normal mío?

**Analista:** Usamos reglas propias, no juicio de la IA: por ejemplo, si hay 3 o más
gastos parecidos y pequeños en la misma categoría en un periodo corto, se marca como
"posible fuga", no como "gasto malo".

**Cliente (IA):** Aceptable, mientras no me diga qué hacer con mi plata, solo que me lo
muestre. Última pregunta: ¿voy a poder ver esto sin conectar mi cuenta bancaria? No
pienso dar esos datos a una app de estudiante.

**Analista:** Correcto, este release no toca bancos ni pagos; todo el registro es manual
por texto.

**Cliente (IA):** Entonces lo mínimo que necesito para probarla es: anotar, ver que
quede bien clasificado, poder corregir si se equivoca, y ver un resumen. Todo lo demás
me da igual por ahora.

---

## Preguntas que quedaron abiertas (cambiarían el diseño)

1. ¿Qué tan seguido se espera que la IA se equivoque en la clasificación? [SUPUESTO: se
   asume una tasa de error aceptable si el usuario puede corregir en 1-2 toques]
2. ¿El umbral de "posible fuga" (3+ gastos similares) debe ser configurable por el
   usuario o fijo en el sistema? [SUPUESTO: fijo para el MVP]
3. ¿Se debe avisar al usuario cuando se detecta una fuga, o basta con mostrarla en el
   dashboard cuando él entre? [Ver HU-07, clasificada como Should]
