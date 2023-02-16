Uso
=====

.. _instalacion:

Instalación
------------

Para el uso de core debe instalar previamente : 


 
Node y NPM Versión LTS 
.. code-block:: console
Empezando
----------------
>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']





cd existing_repo
git remote add origin ``"http://gitlab.xxxxxx.int/xxxxx/c-xxxxx.git"``
git branch -M Developer
git push -uf origin Developer


.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

