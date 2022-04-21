Security Module in Graphenee Flow
=================================

In the security module, we create different users, their groups in which they are categorized and also the policies for these groups.

Add Security to Menu Items
--------------------------

First of all, we will add security menu item in FlowSetup class.

.. code-block:: html
   :linenos:

   @Override
   public List<GxMenuItem> menuItems() {
      items.add(GxMenuItemFactory.securityMenuItem());
      return items;
   }

.. image:: images/secmenu.png


Creating Policies
-----------------

After that, we will create policy.

.. image:: images/policy.png
 :width: 600
 
 Creating Group
 --------------
 
 Then, we will create group.
 
 .. image:: images/group.png
 :width: 600
 
 Creating User
 -------------
 
 At last, we will create the user.
 
 .. image:: images/user.png
 :width: 600
