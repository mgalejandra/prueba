Uso
=====

.. _instalacion:

Instalación
------------

Para el uso de core debe instalar previamente : 


.. code-block:: console

 node y npm versión lts 



Empezando
----------------
>>> cd existing_repo
>>> git remote add origin `http://gitlab.xxxxxx.int/xxxxx/c-xxxxx.git`
>>> git branch -M Developer
>>> git push -uf origin Developer


.. autofunction:: lumache.get_random_ingredients

* npm ``Install``

* npm run ``"dev"``  **ejecucion entorno developer**

* npm run ``"start"`` **ejecucion entorno Producción**



Autenticación
----------------

La interacción con las APIs (todas, sin excepción) necesitan al menos un método de autenticar o validar al cliente,

a partir de ahora explicaremos cómo será el proceso de generación/cofiguración de los headers necesarios para 

que la petición responda correctamente.



**Headers**

El cliente deberá añadir las siguientes cabeceras a cada solicitud:

* api-key: identificador único del cliente
* api-nonce: timestamp de la solicitud
* api-signature: Firma única de la solicitud

**API-KEY**

Es una llave única de 32/64 caracteres generados mediante un patrón aleatorio, y este identifica al cliente sobre el recurso específico.

``api-key: 40caf28d971140f00d33b54f4523390f4568d2384bc9a98afccafe51036cfcc5``


**API-NONCE**

Tiempo UNIX en milisegundos en javascript puede ser generado utilizando Date.now()

``api-nonce: 1670525711124``

**API-SIGNATURE**

El request debe ser firmado usando un algoritmo HMAC basado en sha-384, de esta manera se valida 

que la petición vino de una fuente de confianza y no fué modificado en el proceso. 

El cliente debe obtener el PATH de la petición, el nonce, y el body o query, concatenarlo y firmarlo con el private-key provisto por chinchin.

``api-signature: e12c97270b50302dd33d8ed0c4c27c48302de66bd06721e96dc45fbe82ae014f1c07152c990156df145943ae8b6c5438``



.. autoexception:: lumache.InvalidKindError



