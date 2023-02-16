API
===

.. autosummary::
   :toctree: generated

   **Pago de servicios**



Recarga de saldo 
----------------

..  tip::
     Solicitud encargada de procesar las recargas de saldo por tipo de servicio básico.






``POST  cps/v2/operation/use/pay``




Los tipos de servicios básicos permitidos son:

+------------------------+-----------------+
|  Servicios             |  Id del servicio| 
+========================+=================+
| DIGITEL_PREPAGO:       |       59        | 
+------------------------+-----------------+
| DIGITEL_FIJO:          |        63       |
+------------------------+-----------------+
| DIGITEL_INTERNET:      |        64       |
+------------------------+-----------------+ 
| DIGITEL_POSPAGO:       |       229       |
+------------------------+-----------------+
| MOVISTAR_PREPAGO:      |        57       |
+------------------------+-----------------+
| MOVISTAR_FIJO:         |        62       |
+------------------------+-----------------+
| MOVISTAR_INTERNET:     |        61       |
+------------------------+-----------------+
| MOVISTAR_TV:           |        60       |
+------------------------+-----------------+
| MOVISTAR_POSPAGO:      |        228      |
+------------------------+-----------------+
| MOVILNET_PREPAGO:      |        58       |
+------------------------+-----------------+
| MOVILNET_FIJO:         |        214      |
+------------------------+-----------------+
| SIMPLETV:              |        215      |
+------------------------+-----------------+
| CORPOELEC:             |        216      |
+------------------------+-----------------+
| INTER_PREPAGO:         |        212      |
+------------------------+-----------------+
| INTER_POSPAGO:         |        213      |
+------------------------+-----------------+
| CANTV_RESIDENCIAL:     |        207      |
+------------------------+-----------------+ 
| CANTV_EMPRESAS:        |        209      |
+------------------------+-----------------+ 
| CANTV_ABA:             |        210      |
+------------------------+-----------------+ 
| ABA_ULTRA:             |        211      |
+------------------------+-----------------+ 
| TV_SATELITAL:          |        208      |
+------------------------+-----------------+         



..  note::
      Se debe agregar el código correspondiente al servicio basico que se desea recargar en el parámetro **idTypeService** de la petición.


.. code-block:: console

   Ejemplo de la petición JSON : 

  {
  "numberService": "04243675525",
  "idTypeService": 57,
  "amount": 10
   }



Consulta  de saldo de los servicios
-------------------------------------

..  tip::
     Solicitud encarga de procesar las consultas de saldos de los servicios básicos aplicables.


``GET  /cps/v2/operation/get/balance``



..  note::
      El parámetro **idTypeService** de la solicitud debe tener los mismos codigos que en la petición de recarga de servicios.


      No todos los servicios aplican para consultar saldo, para saber cuales aplican utilizar el endpoint listar servicios básicos
      
      con el queryParam "canGetBalance" con valor "true" y este listará los servicios aplicables para consultar saldo.




+------------------------+----------------------+
|               Query Params                    | 
+========================+======================+
|                        | 02123457654          |
|    numberService       |                      | 
|                        | número del tipo de   |
|                        |  servicio            | 
+-------------------------+---------------------+
|                        | 63                   |
|     idTypeService      |identificador del tipo| 
|                        |de servicio           |
+------------------------+----------------------+