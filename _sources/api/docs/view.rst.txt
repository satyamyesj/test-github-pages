Views
=====

We have different personas for our APIs, namely admin, spender, approver personas.
For each of these person we have BaseView classes like ``AdminView``, ``SpenderView`` e.t.c.

To create new view, we can extend one of these view as show below.

.. code-block:: python
  class CategoryAdminView(AdminView):
    get_schema = GetCategoryAdminSchema
    post_schema = PostCategoryAdminSchema
    def foo(self, name):
      for i in name:
        print(i)
    def bar(self, error):
        raise error
