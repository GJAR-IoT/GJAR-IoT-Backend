# Exportovanie dát

Služba na exportovanie údajov z databázy do formátu CSV. Základná adresa je `/api/export/...` a všetky volania používajú metódu GET.

## Plný export (GET) $\rightarrow$ csv

```
/api/export/all
```

Všetky namerané dáta.

## Plný export jednej miestnosti (GET) $\rightarrow$ csv

```
/api/export/<room_number:int>
```

Všetky dáta z miestnosti `<room_number>`.

## Export jedného dňa z miestnosti (GET) $\rightarrow$ csv

```
/api/export/<room_number:int>/<date:YYYY-MM-DD>
```

Dáta z miestnosti `<room_number>` za deň `<date>`.

## Export rozsahu dátumov z miestnosti (GET) $\rightarrow$ csv

```
/api/export/<room_number:int>/<date_from:YYYY-MM-DD>/<date_to:YYYY-MM-DD>
```

Dáta z miestnosti `<room_number>` v čase medzi `<date_from>` do `<date_to>` (vrátane).

## Export jedného dňa zo všetkých miestností (GET) $\rightarrow$ csv

```
/api/export/all/<date:YYYY-MM-DD>
```

Dáta zo všetkých miestností za deň `<date>`.

## Export rozsahu dátumov zo všetkých miestností (GET) $\rightarrow$ csv

```
/api/export/all/<date_from:YYYY-MM-DD>/<date_to:YYYY-MM-DD>
```

Dáta zo všetkých miestností v čase medzi `<date_from>` do `<date_to>` (vrátane).
