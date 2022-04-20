Different Lists in Graphenee Flow
=================================

GxAbstractEntityList Class
--------------------------

.. code-block:: html
   :linenos:

   public class StudentList extends GxAbstractEntityList<Student> {

   public StudentList() {
      super(Student.class);
   }

   @Override
   protected Stream<Student> getData() {
      return Stream.empty();
   }

   @Override
   protected GxAbstractEntityForm<Student> getEntityForm(Student arg0) {
      return null;
   }

   @Override
   protected void onDelete(Collection<Student> companies) {
   }

   @Override
   protected void onSave(Student company) {
   }

   @Override
   protected String[] visibleProperties() {
   }
}


GxAbstractEntityLazyList Class
------------------------------

.. code-block:: html
   :linenos:

   public class StudentLazyList extends GxAbstractEntityLazyList<Student> {

   public StudentLazyList() {
      super(Student.class);
   }

   @Override
   protected Stream<Student> getData(int arg0, int arg1, Student arg2) {
      return null;
   }

   @Override
   protected int getTotalCount(Student arg0) {
      return 0;
   }

   @Override
   protected GxAbstractEntityForm<Student> getEntityForm(Student arg0) {
      return null;
   }

   @Override
   protected void onDelete(Collection<Student> arg0) {
   }

   @Override
   protected void onSave(Student arg0) {
   }

   @Override
   protected String[] visibleProperties() {
      return null;
   }
}

GxAbstractEntityTreeList Class
------------------------------

.. code-block:: html
   :linenos:

   public class StudentTreeList extends GxAbstractEntityTreeList<Student> {

   public StudentTreeList() {
      super(Student.class);
   }

   @Override
   protected int getChildCount(Student arg0, Student arg1) {
      return 0;
   }

   @Override
   protected Stream<Student> getData(int arg0, int arg1, Student arg2, Student arg3) {
      return null;
   }

   @Override
   protected boolean hasChildren(Student arg0) {
      return false;
   }

   @Override
   protected GxAbstractEntityForm<Student> getEntityForm(Student arg0) {
      return null;
   }

   @Override
   protected void onDelete(Collection<Student> arg0) {
   }

   @Override
   protected void onSave(Student arg0) {
   }

   @Override
   protected String[] visibleProperties() {
      return null;
   }
}
