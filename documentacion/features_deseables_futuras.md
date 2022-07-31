# Features deseables futuras

A fin de securizar el sistema y/o soportar casuísticas adicionales sería deseable soportar algunas o todas de las siguientes features.

#### Filtrado de MAC
Sólo aquellos dispositivos autorizados podrán ser emparejados con un reader.
  
#### Indexación de MAC
El mánager publica un listado de las correspondencias **MAC de dispositivo - Stream de IOTA**.
  
#### Verificación múltiple
Los datos a publicar serán verificados y firmados por múltiples verifiers.
  
#### Quórum de verificación
La validez de un dato publicado requiere de la verificación de m verifiers, siendo m <= n y n el número de verifiers.
                                                                                        
#### Adaptación SSI
En SSI se sigue un patrón:
- Schema: Define en esquema para certificación de datos.
- NYM: Son DID (Decentralized Identifiers) que se escriben en la DLT. En SSI cada uno tiene n DIDs, pero sólo si vas a ser issuer tendrás un NYM (aka, tu DID escrito en DLT) a fin de que cualquiera pueda recuperar su clave pública.
- Schemas ID. Un documento que une Schema+NYM que básicamente se puede interpretar como *La universidad de Jaén (NYM) emite certificados de títulos de ingeniería de informática (schema)*.
- Las certificaciones generadas van asociadas a un Schema ID, por lo que a partir de este campo recuperas la información previa.

En Phonendo seguimos un enfoque similar aunque no equivalente. Seguir un enfome equivalente a SSI ayudaría a la estandarización e interconexión con otras propuestas.
