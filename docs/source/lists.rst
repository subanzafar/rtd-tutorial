Different Grids in Graphenee Flow
=================================

Simple List
-----------

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

Lazy List
---------

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

Tree List
---------

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
- initializeSearchEntity() - Used to initialize the search entity.
- isDragAndDropEnabled() - Return whether drag and drop enable or not.
- isEditable() - Return whether entity is editable or not.
- isGridFilterEnabled() - Return true if filter for grid is enabled.
- isGridInlineEditingEnabled - Return true if inline editing for grid is enabled.
- isRowDraggable() - Return whether the row is draggable or not.
- isSecondaryComponentVisible() - Return true if secondary component is visible.
- onDragEnd() - Invoked when drag in ended.
- onDragStart() - Invoked when drag is started.
- onDrop() - Invoked when component is dropped.
- onGridItemClicked() - Invoked when grid item is clicked.
- onGridItemDoubleClicked() - Invoked when grid item is double clicked.
- onGridItemSelect() - Invoked when grid item is selected.
- preEdit() - Invoked before editing the item.
- refresh() - Used to refresh the list.
- rendererForProperty() - Used to set renderer for given property.
- setColumnVisibility() - Used to set visibility of any column of grid.
- setDragAndDropEnabled() - Used to set drag and drop enabled.
- setEditable() - Used to set if item is editable.
- setRowDraggable() - Used to set the row draggable.
- shouldShowDeleteConfirmation() - Return whether to show confirmation on delete or not. 
- shouldShowExportDataMenu() - Return whether to show export data menu or not.
- shouldShowFormInDialog() - Return whether to show form in dialog or not.
- shouldShowToolbar() - Return whether to show toolbar or not.
- showInDialog() - Return whether to show Indialog or not.
- showSecondaryComponent() - Business logic for showing secondary component.
- showToolbar() - Business logic for showing toolbar.
