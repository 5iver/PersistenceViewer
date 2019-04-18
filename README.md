# PersistenceViewer
Setup:
1) Download the zip file and extract the PersistenceViewer directory to `${OPENHAB_CONF}/html/`.
2) View your persistence data in a browser at `http://[openhab server]:8080/static/PersistenceViewer/`.
3) By default, the Items table will initially be populated with groups that have no parent group. This is good for when all your items are in groups. To initially display all items, add a query string to the end of the URL (?startWithGroups=false), but this will cause the page to load very slowly if you have a lot of items. Alternatively, to initially display a specific group item that holds the items you are persisting, add a query string to the end of the URL (?startItem=gPersist).
4) By default, items will be sorted alphabetically. To disable this, add a query string to the end of the URL (?shouldSort=false). Disabling the sort will also dramatically improve performance if you use startWithGroups=false or if your startItem is a group with a lot of items in it.
5) By default, the default persistence service configured in OH is used. To use a different one, add a query string to the end of the URL (?serviceId=rrd4j).

Query strings need to be separated by an ampersand. The only part of the querystrings that is case sensitive is the value for startItem. Here is an example (they can be used in any order)...

http://[openhab server]:8080/static/PersistenceViewer/?SeRvIcEiD=MaPdB&ShOuLdSoRt=FaLsE&StArTiTeM=gPersistence

Usage:
1) By default, one month of persistence data will be retrieved, unless specific dates are entered in the Start and End date fields.
2) Groups will have a green background and items will have a grey background.
3) When a group or item is selected, the persistence data will be displayed. When a group is selected, its items will also be displayed in the Items table. If no data is available, N/A will be displayed.
4) Use the breadcrumbs to navigate backwards.
5) PersistenceViewer can be displayed in HABpanel by adding it into a Frame widget, but this may not work well for lower resolution screens or if the widget is too small.

Please comment in the OH community forum... https://community.openhab.org/t/persistenceviewer/46407
