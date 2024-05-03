Views
=====

We have BaseView classes like ``SuperAdminView``, ``StudentView`` e.t.c.

-------------------
Creating View Class
-------------------

To create new view, we can extend one of these view as show below.

.. code-block:: python

  class SettingsSuperAdminView(SuperAdminView):
    get_schema = GetSettingsSuperAdminSchema
    post_schema = PostSettingsSuperAdminSchema
    def foo(self, name):
      for i in name:
        print(i)
    def bar(self, error):
        raise error
