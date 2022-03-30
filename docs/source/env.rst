Setting up the environment
==========================

Prerequisites
-------------
- VS Code or Eclipse
- Project created in Java Spring Boot or `Start new project <https://spring.io/guides/gs/spring-boot/>`_

.. note::

   You need to install Lombok extension to use Spring Boot & Spring JPA annotations inside VS Code or Eclipse.

Adding Graphenee
----------------
First, add graphenee version to properties tag in pom.xml file at root of your project:

.. code-block:: html
   :linenos:

   <properties>
         <graphenee.version>3.5.0-SNAPSHOT</graphenee.version>
   </properties>
   
