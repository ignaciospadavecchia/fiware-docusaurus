## **¿Qué es FIWARE?**
    
    FIWARE es un *framework* de componentes de código abierto que proporciona bloques modulares de construcción (llamados “facilitadores genéricos” o *generic enablers*) que pueden combinarse e integrarse a componentes de terceros para desarrollar de plataformas y soluciones inteligentes, y operar en un ciclo continuo de retroalimentación de captura de datos, procesamiento de información y actuación de cambios en el mundo real.
    

## **¿Qué es un Context Broker?**
    
    En el corazón de una arquitectura FIWARE siempre hay un **Gestor de Contexto** o *Context Broker*. La implementación más madura de este *generic enabler* fue desarrollada por Telefónica con el nombre clave **Orion**. Orion basicamente expone una API construida sobre [la especificación original de NGSI version 2](http://telefonicaid.github.io/fiware-orion/archive/api/v2/), y añade un gran número de mejoras. [*]
    
    *[*] La API de Orion es totalmente compatible con la especificación original NGSIv2 aunque algunas pequeñas diferencias se describen en este [anexo](https://github.com/telefonicaid/fiware-orion/blob/master/doc/manuals/orion-api.md#differences-regarding-the-original-ngsiv2-spec).*
    

## **¿Qué es una API NGSIv2?**
    
    Una **API NGSIv2 (Next Generation Service Interface version 2)** define:
    
    - **un modelo** de datos para la información de contexto, basado en un modelo de información simple que utiliza la noción de `entidades de contexto`;
    - **una interfaz de datos de contexto** para intercambiar información mediante operaciones de `consulta, suscripción` y `actualización`;
    - **una interfaz de disponibilidad** **de datos de contexto** para intercambiar información sobre cómo obtener información de contexto.

## **¿Qué son las entidades de contexto?**
    
    Una entidad representa una cosa, es decir, cualquier objeto físico o lógico (por ejemplo, un sensor, una persona, una habitación, etc.). Cada entidad tiene un **ID de entidad** y un **tipo de entidad** que describe semánticamente lo que representa. Es requerimiento para una entidad que se identifique de manera única por la combinación de su `ID` y `tipo`.
    

## **¿Qué son los atributos de contexto?**
    
    Los atributos de contexto son propiedades de las entidades. En el modelo de datos NGSI, los atributos tienen:
    
    - Un **nombre** que describe qué propiedad representa
    - Un **tipo** que representa el tipo de valor dentro del modelo NGSI.
    - Un **valor** que contiene los datos reales.
    - **Metadatos** opcionales que describen propiedades del valor del atributo como `precisión`, `proveedor` o `timestamp`.

## **¿Qué son los metadatos de contexto?**
    
    Los metadatos de contexto se utilizan en varios lugares de FIWARE NGSI. Cada metadato tiene:
    
    - Un **nombre** que describe su función
    - Un **tipo** que describe el tipo de valor dentro del modelo NGSI
    - Un **valor** que contiene los metadatos reales
    
    No está previsto que los metadatos contengan metadatos anidados.