# Prototipo de scrollytelling

Una sola página, con el contenido **cifrado**. Hace falta la clave para abrirla.

## Qué es esto, y qué no

Lo que está publicado aquí es texto cifrado (AES-GCM, con la llave derivada de
la clave por PBKDF2 con 310,000 iteraciones). Sin la clave no hay nada que leer:
ni en «ver código fuente», ni en un buscador. La página tampoco pide nada a
ningún servidor: todo viaja dentro del archivo.

**Pero esto no es control de acceso.** Quien tenga la clave puede reenviarla, y
quien tenga el archivo puede intentar adivinarla sin límite de intentos. Sirve
para compartir un borrador con un grupo pequeño, no para proteger material de
alguien que lo busque.

**Es un borrador de trabajo. No publicar ni reenviar.**

## Cómo se genera

Desde el repositorio de trabajo:

```
node scripts/publicar_scrolly.mjs <clave> outputs/publicado
```

Cambiar la clave es volver a correr eso y volver a subir el `index.html`.
