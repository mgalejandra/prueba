API
===

.. autosummary::
   :toctree: generated

   **Pago de servicios**



Contenido
--------

/cps/v2/operation/use/pay

Solicitud encargada de procesar las recargas de saldo por tipo de servicio básico.



  DIGITEL_PREPAGO: 59
  DIGITEL_FIJO: 63
  DIGITEL_INTERNET: 64
  DIGITEL_POSPAGO: 229
  MOVISTAR_PREPAGO: 57
  MOVISTAR_FIJO: 62
  MOVISTAR_INTERNET: 61
  MOVISTAR_TV: 60
  MOVISTAR_POSPAGO: 228
  MOVILNET_PREPAGO: 58
  MOVILNET_FIJO: 214
  SIMPLETV: 215
  CORPOELEC: 216
  INTER_PREPAGO: 212
  INTER_POSPAGO: 213
  CANTV_RESIDENCIAL: 207
  CANTV_EMPRESAS: 209
  CANTV_ABA: 210
  ABA_ULTRA: 211
  TV_SATELITAL: 20



  Se debe agregar el código correspondiente al servicio basico que se desea recargar en el parámetro idTypeService de la petición.



  {
  "numberService": "04243675525",
  "idTypeService": 57,
  "amount": 10
}