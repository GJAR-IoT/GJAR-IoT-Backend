# Exporting data

Service for exporting data from the database as CSV files. Base address is `/api/export/...`, and all API calls use GET.

## Full export (GET) → csv

```
/api/export/all
```

All measured data.

## Full export of a specific room (GET) → csv

```
/api/export/<room_number:int>
```

All data from the room `<room_number>`.

## One day export of a specific room (GET) → csv

```
/api/export/<room_number:int>/<date:YYYY-MM-DD>
```

Data from the room `<room_number>` from `<date>`.

## Range of days export from a room (GET) → csv

```
/api/export/<room_number:int>/<date_from:YYYY-MM-DD>/<date_to:YYYY-MM-DD>
```

Data from the room `<room_number>` between `<date_from>` and `<date_to>` (inclusive).

## One day export of all rooms (GET) → csv

```
/api/export/all/<date:YYYY-MM-DD>
```

Data from all rooms from `<date>`.

## Range of days export from all rooms (GET) → csv

```
/api/export/all/<date_from:YYYY-MM-DD>/<date_to:YYYY-MM-DD>
```

Data from all rooms between `<date_from>` and `<date_to>` (inclusive).
