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
- getData() will take list of entity.
- getEntityForm() will return the form which is autowired.
- We will inject our service here to use crud methods.
- visibleProperties() - In this method, we will specify the columns that will be displayed in list. Column names here must match with attribute names of model.

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

- getTotalCount() will take the length / count of list of entity. 

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
- getChildCount() will take the count of child entites related to list.
- hasChildren() will take boolean i.e. if there're any child entites.

List Customization
------------------

Here we will discuss about different methods that are being used for customizing lists in graphenee.

- availableProperties() - Used to get the available properties of grid.
- columnFilterForProperty() - Used to implement filter for any property of grid.
- customizeAddMenuItem() - Used to customzie add menu item button.
- customizeDeleteMenuItem() - Used to customzie delete menu item button.
- customizeEditMenuItem() - Used to customzie edit menu item button.
- dataProvider() - Used to implement data provider for current entity. 
- decorateColumn() - Used to customzie column.
- decorateGrid() - Used to customize grid.
- decorateMenuBar() - Used to customzie menu bar.
- decorateSearchForm() - Used to customize search form.
- decorateToolbarLayout() - Used to customize toolbar layout.
- dialogHeight() - Used to set dialog height.
- dialogWidth() - Used to set dialog width.
- disableShortcuts - Used to disable shortcuts for list.
- dismissDialog() - Used to dismiss the opened dialog.
- editItem() - Invoked when item is being edited.
- enableShortcuts() - Used to enable shortcuts for list.
- entityGrid() - Returns the grid for given entity.
- exportData() - Used to implement business logic for exporting data. 
- getSearchEntity() - Used to get current entity.
- hideSecondaryComponent() - Used to hide secondary component of list.
- hideToolbar() - Used to hide toolbar.
initializeSearchEntity
isDragAndDropEnabled
isEditable
isGridFilterEnabled
isGridInlineEditingEnabled
isRowDraggable
isSecondaryComponentVisible
onDragEnd
onDragStart
onDrop
onGridItemClicked
onGridItemDoubleClicked
onGridItemSelect
preEdit
refresh
rendererForProperty
setColumnVisibility
setDragAndDropEnabled
setEditable
setOnSingleItemSelect
setRowDraggable
shouldShowDeleteConfirmation
shouldShowExportDataMenu
shouldShowFormInDialog
shouldShowToolbar
showInDialog
showSecondaryComponent
showToolbar
