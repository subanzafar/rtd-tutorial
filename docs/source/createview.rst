Creating a view in Graphenee
============================
Every class related to a view will be created inside ``/vaadin/`` folder.

MainLayout Class
----------------

.. code-block:: html
   :linenos:

   @Push
   public class MainLayout extends GxAbstractAppLayout {
   
      @Autowired
      GxAbstractFlowSetup flowSetup;

      @Override
      protected GxAbstractFlowSetup flowSetup() {
         return flowSetup;
      }
   }

HomeView Class
--------------

.. code-block:: html
   :linenos:

   @GxSecuredView
   @Route(value = "", layout = MainLayout.class)
   public class HomeView extends GxVerticalLayoutView {
      //any default component can be displayed
   }
   
LoginView Class
---------------

.. code-block:: html
   :linenos:

   @Route(value = "login")
   public class LoginView extends GxAbstractLoginView {

      @Autowired
      GxAbstractFlowSetup flowSetup;

      @Override
      protected GxAbstractFlowSetup flowSetup() {
         return flowSetup;
      }

      @Override
      protected GxAuthenticatedUser onLogin(LoginEvent event)
            throws AuthenticationFailedException, PasswordChangeRequiredException {
         return new MockUser();
      }
   }
   
FlowSetup Class
---------------

.. code-block:: html
   :linenos:

   @Component
   @VaadinSessionScope
   public class FlowSetup extends GxAbstractFlowSetup {

      @Override
      public List<GxMenuItem> menuItems() {
         List<GxMenuItem> items = new ArrayList<>();
         // we will add menu items later.
         return items;
      }

      @Override
      public Class<? extends RouterLayout> routerLayout() {
         return MainLayout.class;
      }

      @Override
      public String appTitle() {
         return "Testing Portal";
      }

      @Override
      public String appVersion() {
         return "1.0";
      }
   }
