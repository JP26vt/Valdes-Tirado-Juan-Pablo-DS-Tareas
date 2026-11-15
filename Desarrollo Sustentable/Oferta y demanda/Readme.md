# Nombre del proyecto
Oferta y demanda.

## Descripción
En una economía de mercado el precio de un producto se fija donde se cruzan la oferta (cuánto
quieren vender los productores) y la demanda (cuánto quieren comprar los consumidores). Cuando
la oferta cae por una veda o una mala temporada, el precio sube; cuando hay sobreproducción,
baja.
En esta práctica el equipo construye un simulador físico: dos potenciómetros representan la oferta y
la demanda de un kilo de camarón, el Arduino calcula el precio de equilibrio, lo muestra en su matriz
LED y, cuando detecta escasez, envía una alerta a Telegram a través de Make.

## Objetivos de aprendizaje
Que el alumno explique cómo la oferta y la demanda fijan los precios, relacione la escasez de un
recurso natural con su precio, y construya un sistema IoT que convierta un fenómeno económico en
datos y alertas automáticas.

## Material utilizado
Make y sus herramientas
 

>


## Código
[Main.txt](https://github.com/JP26vt/Valdes-Tirado-Juan-Pablo-DS-Tareas/blob/main/Desarrollo%20Sustentable/Huella%20energetica/Codigo/Main.txt)


## Imagenes
<img width="1261" height="412" alt="Captura de pantalla 2026-11-12 115135" src="https://github.com/user-attachments/assets/39b9f511-0878-43c5-85c5-1c4d376683da" />

 <img width="1320" height="477" alt="Captura de pantalla 2026-11-12 115254" src="https://github.com/user-attachments/assets/dcab111b-19b0-4a8a-96cf-33513ba0ce2b" />







## Video del funcionamiento

[Readme](https://github.com/JP26vt/Valdes-Tirado-Juan-Pablo-DS-Tareas/tree/main/Desarrollo%20Sustentable/Huella%20energetica/Video)

[Ver video en YouTube]https://youtu.be/73fWhuESxQY?si=NVZ-p-2CVh7_rjlu



## Conclusiones
En esta práctica vimos de forma directa cómo se forma el precio de un producto en una economía de mercado. Al mover los potenciómetros, la demanda y la oferta de un kilo de camarón cambiaban el precio de equilibrio en tiempo real. Cuando la demanda subía o la oferta bajaba, el precio aumentaba. Cuando la oferta crecía, el precio caía. Esto confirma que el precio no depende solo del producto, sino de cuánto quieren comprar los consumidores y cuánto están dispuestos a vender los productores.

##Preguntas de reflexion
1. ¿Por qué el precio sube cuando la oferta baja, aunque el producto sea el mismo?
El precio sube porque su valor en el mercado no depende solo de lo que cuesta producir el camarón, sino de qué tan escaso es en relación con la cantidad de personas que lo quieren comprar. Cuando la oferta baja, por ejemplo por una veda, un huracán o una mala temporada, hay menos kilos disponibles para la misma cantidad de compradores. Si la demanda se mantiene igual o incluso aumenta, como en Semana Santa, los consumidores compiten por un producto más escaso, y los vendedores se dan cuenta de que pueden pedir un precio más alto sin quedarse sin clientes.

2. Una veda reduce la oferta y sube el precio. ¿Por qué aun así conviene para la economía de largo plazo?
La veda conviene porque el camarón es un recurso natural renovable, pero solo si se le permite reproducirse y crecer. Si se pescara sin parar, incluso durante la época de reproducción, se capturarían ejemplares pequeños o hembras antes de que dejen crías, y cada temporada habría menos camarón.

3. ¿Qué factores reales de la oferta de camarón no considera su modelo (clima, costos de combustible, importaciones)?
Nuestro modelo es una simplificación, porque la oferta depende solo de la posición del potenciómetro y el precio se calcula con una fórmula lineal. En la realidad, la oferta de camarón la determinan muchos factores que el simulador no toma en cuenta.

4. ¿Qué ventaja tiene automatizar una alerta de escasez para un productor o una cooperativa?
La principal ventaja es que el productor se entera de un cambio en el mercado en el momento en que ocurre, sin tener que estar revisando precios o datos todo el día. En nuestra práctica, cuando la demanda superaba a la oferta por 25 puntos o más, el sistema mandaba un mensaje a Telegram con la demanda, la oferta y el precio de equilibrio. Una cooperativa podría recibir un aviso parecido directamente en el celular de sus socios.

5. ¿El precio de mercado incluye el costo ambiental de producir el camarón? Expliquen.
En general, no. El precio de mercado refleja lo que cuesta producir y llevar el camarón al consumidor (combustible, mano de obra, alimento, transporte, ganancia) y lo que la gente está dispuesta a pagar, pero casi nunca incluye el daño que esa producción causa al ambiente. En economía a esos costos que no se pagan en el precio se les llama externalidades negativas: los provoca el productor, pero los asume la sociedad y la naturaleza.

## Resultados
[Resultados.pdf](https://github.com/JP26vt/Valdes-Tirado-Juan-Pablo-DS-Tareas/blob/main/Desarrollo%20Sustentable/Huella%20energetica/Resultados/Resultados%20Huella%20Energ%C3%A9tica.pdf)


Este documento contiene la descripción de la práctica, objetivos y procedimientos realizados.

- Reporte técnico estilo IEEE (PDF)
- Datos CSV (si aplica)
- Diagramas adicionales
