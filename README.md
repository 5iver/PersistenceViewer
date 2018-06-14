# PersistenceViewer
HTML/jQuery/AJAX page for viewing openHAB persistence data

Setup:
1) Copy the PersistenceViewer folder to openHAB {%openhab%}/conf/html.
2) By default, all items will be displayed. To select a group item that holds the items you are persisting, edit index.html and set startItem to the name of the item on line 155.
3) By default, items will be sorted alphabetically. To disable this, edit index.html and set shouldSort to false on line 156.
4) By default, the default persistence service is used. To set a specific persistence service, edit index.html and set persistenceService on line 157.
5) View your persistence data in a browser at http://<openhab server>:8080/static/history.

Usage:
1) By default, one month of persistence data will be retrieved, unless specific dates are entered in the Start and End date fields.
2) Groups will have a green background and items will have a grey background.
3) When a group is selected, it's persistence data will be displayed, along with all of the items in the group. If no data is available, N/A will be displayed.
4) Use the breadcrumbs to navigate backwards.
5) PersistenceViewer can be displayed in HABpanel by adding it into a Frame widget, but this may not work well for lower resolution screens or if the widget is too small.
