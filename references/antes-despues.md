# Antes / después

Traducciones cortas de cada principio a una pantalla concreta. El «antes» no es un hombre de paja:
es lo que sale por defecto cuando nadie decidió nada. El «después» es la misma pantalla con una
decisión tomada.

Todos pasan el filtro de §7 de la skill: **nada grita, nada bloquea, todo informa, nada se repite
hasta volverse ruido**.

---

## A1 · `instant emotional feedback`

### Guardar algo que se guarda cuarenta veces al día

```diff
- toast gris arriba a la derecha: "Guardado"  ·  3 s  ·  lejos de donde se tocó
+ el propio botón confirma en su sitio: el icono pasa a palomita con un rebote corto,
+ el botón se tiñe un punto, y vuelve a su estado en ~1 s. Sin toast, sin bloquear.
```

**Por qué:** la retroalimentación llega **donde estaba la atención**. Un toast al otro extremo de
la pantalla obliga a buscarlo; la mitad de las veces nadie lo ve y la acción se siente huérfana.

### Marcar un hábito del día

```diff
- la casilla cambia de vacía a marcada. Fin.
+ la casilla se llena desde el centro, la fila se asienta medio paso,
+ y el contador del mes sube con ella. Un gesto, tres confirmaciones encadenadas.
```

---

## A2 · `celebrate small wins`

```diff
- "Has completado 7 de 7." (texto, mismo cuerpo que todo lo demás, mismo gris)
+ el contador llega a 7/7 y la fila entera se asienta con un brillo breve;
+ debajo, una línea escrita a propósito para ESTE momento: "Semana completa."
+ Pequeño, pero claramente decidido. No confeti.
```

**La prueba de fuego:** ¿esta pantalla de éxito se podría usar tal cual para otros cinco éxitos
distintos? Si sí, es genérica. Un estado de éxito **no tiene que ser enorme, pero sí intencional**.

---

## A3 · `use character expressions`

```diff
- la mascota aparece siempre igual, de brazos cruzados, en la esquina de la pantalla vacía.
+ la mascota REACCIONA: asiente al acertar, ladea la cabeza al fallar,
+ y en la pantalla vacía mira hacia el botón que hay que pulsar.
+ Tres expresiones bien hechas valen más que veinte poses estáticas.
```

**Si no tienes mascota, no la inventes para esto.** El principio es que las emociones se contagian,
y hay otras formas de aplicarlo (una copia que responde al estado real, un color que acompaña).
Añadir un personaje porque lo dice una lista es exactamente el tipo de apéndice que se nota.

---

## A4 · `progress animations`

```html
<!-- ANTES: el valor aparece ya puesto. El usuario ve un estado. -->
<div class="barra" style="width: 60%"></div>
```

```html
<!-- DESPUÉS: el valor LLEGA. El usuario ve lo que ha construido. -->
<div class="barra" style="--de: 45%; --a: 60%"></div>
<!-- la barra crece de --de a --a al entrar en pantalla,
     y el número de al lado cuenta hasta su cifra -->
```

**El detalle que importa:** se anima **desde el valor anterior**, no desde cero. Desde cero es una
animación de carga; desde el valor anterior es progreso, que es lo que el principio pide.

---

## B1 · `polish builds trust`

```diff
- al cargar, la pantalla salta: primero el esqueleto, luego el saldo aparece y empuja
- todo hacia abajo; el botón queda 8 px desalineado con la tarjeta de arriba.
+ el hueco del saldo ya está reservado con su altura final: al llegar el dato,
+ nada se mueve de sitio. El botón se alinea con el borde de la tarjeta.
```

**Por qué esto es una señal de confianza y no una manía:** en una pantalla de dinero, un salto de
maquetación se lee como «esto lo hicieron a medias». La gente no lo razona, lo siente — y lo que
siente es riesgo. Cada micro-interacción es una señal de confianza.

---

## B2 · `keep it approachable`

```diff
- "Error: fondos insuficientes para cubrir la comisión de red (gas)."
+ "Te faltan $3.200 para cubrir el costo de envío de esta operación.
+  Agrega saldo y lo volvemos a intentar."  [Agregar saldo]
```

**Lo que cambió:** el tono dejó de añadir tensión a un momento que ya la tenía, y el mensaje
termina en una salida. Hacer un tema pesado más ligero **no es trivializarlo**: es no cargarlo más.

---

## B3 · `build for people, not just pros`

```diff
- un campo "Dirección de la billetera" con un pegado de 42 caracteres y nada más.
+ el mismo campo, pero: valida al pegar y dice en claro "Dirección válida";
+ si es la primera vez, una línea explica de dónde se saca; y si el usuario
+ pega algo que no lo es, el error dice QUÉ pegó, no solo que está mal.
```

**La regla:** no asumas que el usuario conoce las reglas. Si un paso solo tiene sentido para quien
ya sabía, ese paso está escrito para la persona equivocada.

---

## B4 · `performance < product feel`

```diff
- "Confirmar" → spinner centrado en una capa gris sobre toda la pantalla → pantalla nueva.
+ "Confirmar" → el botón se convierte en la barra de progreso de la propia operación
+ (la espera está DENTRO del botón que se pulsó) → la misma pantalla se resuelve
+ en el comprobante, sin salto ni parpadeo.
```

**Lo que se gana:** la espera deja de ser un agujero y pasa a ser parte del gesto. El vídeo mete
explícitamente el «esperar» entre las cosas que se **sienten**, junto a tocar y deslizar.

---

## C1 · `nail the first impression`

```diff
- registro: 6 campos en una página, el logo arriba, el botón azul por defecto,
- y al terminar un "¡Listo!" sobre una pantalla vacía.
+ un paso a la vez, con transición suave entre ellos; el primer paso pide SOLO
+ lo que no se puede deducir; el cierre no es "Listo", es la primera pantalla real
+ ya con algo del usuario dentro.
```

**Por qué pesa tanto:** es donde se comunica calidad, confianza y cuidado **antes de que el
producto haya hecho nada**. Si el primer minuto se siente genérico, todo lo demás nace cuesta
arriba.

---

## C2 · `add moments of delight`

```diff
- la lista aparece entera de golpe al cargar.
+ las filas entran escalonadas unos milisegundos entre sí. No se percibe como animación:
+ se percibe como que la pantalla "se asienta". Nadie lo nombrará, y ese es el punto.
```

**El listón:** si un usuario puede señalarlo y decir «qué bonito eso», ya es demasiado. El efecto
es la suma silenciosa, no la pieza.

---

## C3 · `make interactions feel dynamic`

```diff
- gráfica estática del gasto del mes, con leyenda y tooltip al pasar el ratón.
+ se arrastra el dedo sobre la gráfica y el punto bajo el dedo se ilumina:
+ la cifra grande de arriba cambia con él. El número deja de ser un dato
+ y pasa a ser algo que se manipula.
```

```diff
- la tarjeta del cliente es un PNG plano en una tarjeta blanca.
+ la tarjeta responde al puntero con una inclinación mínima y un brillo que la recorre.
+ Un momento, no un juguete: al soltar vuelve a su sitio y no vuelve a llamar la atención.
```

---

## Un «después» que está mal

Para calibrar el filtro, el caso contrario:

```diff
  "Pago recibido"
- una palomita que crece y se asienta en ~400 ms. Luego el comprobante.
+ CONFETI a pantalla completa durante 2 s, un sonido, y el botón de continuar
+ deshabilitado hasta que la animación termina.
```

Falla **las cuatro** preguntas del filtro: se puede nombrar, bloquea, no informa de nada que la
palomita no dijera, y como el pago es rutinario se repetirá hasta volverse ruido. **Aquí el
"antes" era el bueno.**
