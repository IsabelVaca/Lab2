

## Ejercicio 0 Clasifica

| # | Responsabilidad | ¿Qué capa? |
|---|---|---|
| 1 | Calcular el promedio de estrellas de un restaurante | dominio |
| 2 | Mostrar `4.333…` como `"4.3"` | UI |
| 3 | La lista de los restaurantes de muestra | datos |
| 4 | "El comentario debe tener al menos 15 caracteres" | dominio |
| 5 | El botón "Publicar" se pinta gris | UI |
| 6 | Recordar cuántas estrellas lleva marcadas el usuario | VM |
| 7 | Decidir a qué pantalla ir después de guardar | UI |
| 8 | Convertir `priceLevel = 2` en `"$$"` | dominio |

## Ejercicio B2 

**Rompimiento 1 — Cambia `type = NavType.IntType` por `StringType` sin tocar `getInt`:**
Al tocar el restaurante aparece en blanco la pantalla. El tema es que se espera un int por (`getInt`), no crashea pero no funciona bien.

**Rompimiento 2 — Toca la misma tarjeta 5 veces rápido y luego "atrás" 5 veces:**
La pantalla del restaurante se traba y tienes que picarle salir varias veces, se llama a la pantalla muchas veces y quedan apiladas.

## Ejercicio B4 
**1. ¿Cuál de las tres pruebas de la Parte 0 detecta este error?**
La 1 y la 3. Cuando sales y regresas desaparece la reseña que es una falla, si giras el teléfono también pasa lo mismo.

**2. ¿A quién le pertenecen las reseñas: al detalle, a la lista, o a ninguno de los dos? Justifica con lo que pasa cuando el promedio debe verse también en la tarjeta de la lista.**
Le pertenece a los dos o a algo superior a ellas, ambos deben estar enterados de eso para que si algo cambia se refleja en la otra.

**3. Si movieras las reseñas a un `remember` en `SaboresApp()` —el Composable que contiene al `NavHost`— ¿se arregla el Experimento 1? ¿Y el 2?**
Uno sí pero el otro no, al girar el dispositivo se vuelve a crear todo y se borra todo todavía.
