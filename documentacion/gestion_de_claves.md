# Gestión de claves

En phonendo existen diferentes servicios que operan con los datos, existiendo a su vez múltiples pares de claves asimétricas que son empleadas para la verificación de la información y su publicación en IOTA. Específicamente:
1. Reader sólo comunica datos al manager indicando la MAC del dispositivo, no existiendo ninguna protección en los datos.
2. Manager deriva para cada MAC una clave privada que será usada para la publicación de un stream. Esta clave privada se deriva combinando el MAC con una semilla (<pk> = f(seed, mac)), por lo que las instalaciones que compartan semilla publicarán en los mismos streams.
3. El verifier tiene su propia identidad (pk) que estará publicada en IOTA (similar a un DID SSI indicando que es un verificador/certificador de información valida).
4. Los datos que escribe el publisher van asociados al stream de la private key creada en 2 para el device y cada uno de los paquetes va con la firma de 3.
5. Opcionalmente el publisher puede decidir si publicar en el stream datos firmados por el verifier o no (eso al gusto, no aporta mayor ni menor seguridad).

#### Resumen
1. Manager es quien gestiona las identidades de los dispositivos en su instalación y sus correspondientes streams.
2. Verifier es quien garantiza la validez de los datos. Las identidades de los verifier son públicas y conocidas para que cualquiera ente externo pueda conocer quién fue el que 'endorsó' la confianza en el dato.
