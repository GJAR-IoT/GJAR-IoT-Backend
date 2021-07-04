# APIv2 Volania

Táto časť popisuje volania na server. Jednotlivé volania sú HTTP požiadavky s metódou GET alebo POST, ktoré môžu obsahovať údaje vo formáte JSON. To je zároveň aj formát návratovej hodnoty volaní.

## Identifikácia Nodov

Každý Node má priradený jedinečný indentifikátor - **token**. Je to reťazec znakov, ktorý je potrebný na identifikáciu Nodu pri niektorých volaniach.

## Záznam merania

```
/api/v2/data
```

Slúži na odoslanie dát z merania serveru.
Obsahuje polia vo formáte:

```json
{
	token: str,
	? temperature: float,
	? humidity: float,
	? brightnedd: int
}
```

kde `?` znamená, že pole je nepovinné. Vracia iba to, či bola operácia úspešná.

## Požiadavka dát

```
/api/v2/view
```

Slúži na získanie údajov zo servera.
Obsahuje polia:

```json
{
	room: int,
	time_from: str (čas vo formáte ISO 8601: "YYYY-MM-DD hh:mm:ss")
	time_to: str (ISO 8601)
}
```

a vracia JSON vo formáte:

```json
{
	status: str,
	room: int,
	data: /* zoznam objektov */
		[{
			time: str (ISO 8601),
			temperature: str (obsahujúci float),
			humidity: str (obsahujúci float),
			brightness: str (obsahujúci float)
		}]
}
```
