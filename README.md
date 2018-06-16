# PersistenceViewer
Setup:
1) Copy the PersistenceViewer directory to openHAB {%openhab%}/conf/html.
2) View your persistence data in a browser at http://[openhab server]:8080/static/PersistenceViewer/.
3) By default, all items will be displayed. To select a group item that holds the items you are persisting, add a queryString to the end of the URL (?startItem=gPersist).
4) By default, items will be sorted alphabetically. To disable this, add a queryString to the end of the URL (?shouldSort=false).
5) By default, the default persistence service configured in OH is used. To use a different one, add a querystring to the end of the URL (?serviceId=rrd4j).

QueryStrings need to be separated by an ampersand, and the query part (startItem, shouldSort, serviceId) are case sensitive. The values for shouldSort and serviceId are not case sensitive. The Here is an example using all of them (they can be put in any order)...
http://[openhab server]:8080/static/PersistenceViewer/?startItem=gPersistence&shouldSort=FaLsE&serviceId=MaPdB.

Usage:
1) By default, one month of persistence data will be retrieved, unless specific dates are entered in the Start and End date fields.
2) Groups will have a green background and items will have a grey background.
3) When a group or item is selected, the persistence data will be displayed. When a group is selected, its items will also be displayed in the Items table. If no data is available, N/A will be displayed.
4) Use the breadcrumbs to navigate backwards.
5) PersistenceViewer can be displayed in HABpanel by adding it into a Frame widget, but this may not work well for lower resolution screens or if the widget is too small.

Please comment in the OH community forum... https://community.openhab.org/t/persistenceviewer/46407
