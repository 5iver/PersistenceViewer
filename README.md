# PersistenceViewer
HTML/jQuery/AJAX page for viewing openHAB persistence data

1) Copy the PersistenceViewer folder to openHAB {%openhab%}/conf/html.
2) By default, all items will be displayed. To select a group item that holds the items you are persisting, edit index.html and set startItem to the name of the item on line 155.
3) By default, items will be sorted alphabetically. To disable this, edit index.html and set shouldSort to false on line 156.
4) By default, the default persistence service is used. To set a specific persistence service, edit index.html and set persistenceService on line 157.
5) View your persistence data in a browser at http://<openhab server>:8080/static/history.
