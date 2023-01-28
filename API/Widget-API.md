# vtkWidgetManager
- Manages how, when, and where widgets appear within a view.
- There may be only one `vtkWidgetManager` per view.
- To create a link between the widget manager and a view use: `widgetManager.setRenderer(renderer);`