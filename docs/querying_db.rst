Querying DB
===========

Below sections describes different ways to query DB.


=================
Writing raw query
=================

To write below SQL as raw query you can use ``db_session`` object.

.. code-block:: psql
  with c1 as (
    select
      id, count(*)
    from
      example_table
    where
      col = value
    group by
      id
  )
  select * from c1;
.. code-block:: python
  from db import db
  raw_query = "<above query>"
  result = db.session.execute(raw_query)