# Taller raster

## Propósito

Comprender algunos aspectos fundamentales del paradigma de rasterización.

## Tareas

Emplee coordenadas baricéntricas para:

1. Rasterizar un triángulo;
2. Implementar un algoritmo de anti-aliasing para sus aristas; y,
3. Hacer shading sobre su superficie.

Implemente la función ```triangleRaster()``` del sketch adjunto para tal efecto, requiere la librería [frames](https://github.com/VisualComputing/framesjs/releases).

## Integrantes

Máximo 3.

Complete la tabla:

|    Integrante    | github nick |
|------------------|-------------|
| Eduardo Galeano  | cegard     |
| Jhonatan Guzmán  | Jhonnyguzz    |

## Discusión

Describa los resultados obtenidos. Qué técnicas de anti-aliasing y shading se exploraron? Adjunte las referencias. Discuta las dificultades encontradas.

Rasterización: https://elcodigografico.wordpress.com/2014/03/29/coordenadas-baricentricas-en-triangulos/ - Se describe el proceso usando la norma del vector.

Antialiasing: [Artículo de Microsoft](https://msdn.microsoft.com/en-us/library/windows/desktop/cc627092)
https://en.wikipedia.org/wiki/Multisample_anti-aliasing

Se emplea la técnica de Multisampling que consiste en tener de muestra subpixeles y así dar una opacidad al pixel según el número total de subpixeles dentro del triángulo. En total se usaron 4 subpixeles por pixel.

Shading: https://www.scratchapixel.com/lessons/3d-basic-rendering/ray-tracing-rendering-a-triangle/barycentric-coordinates

Las coordenadas baricéntricas sirven para muchos factores del tríangulo como el color, si suponemos que a cada vértice le corresponde un color RGB es fácil encontrar el color correspondiente de cada pixel dentro del triángulo usando el alpha, theta y gamma descritos en el link de rasterización.

La mayor dificultad fue trabajar con la librería frames para obtener las coordenadas (x,y) de los puntos y vértices para aplicar las fórmulas. 

## Entrega

* Modo de entrega: [Fork](https://help.github.com/articles/fork-a-repo/) la plantilla en las cuentas de los integrantes (de las que se tomará una al azar).
* Plazo: 1/4/18 a las 24h.
