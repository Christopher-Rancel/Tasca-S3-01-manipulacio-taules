# Exercici 2 - Actualització IBAN

## El departament de Recursos Humans ha identificat un error en el número de compte associat a la targeta de crèdit amb ID CcU-2938. La informació correcta és TR323456312213576817699999. Mostra que el canvi s’ha realitzat.

## Descripció
En aquest exercici s’ha corregit un error en el camp `iban` d’una targeta de crèdit concreta dins la taula `credit_card`.  
L’objectiu és actualitzar el valor incorrecte i verificar que el canvi s’ha aplicat correctament.

---

## Actualització de dades

S’ha actualitzat el valor del camp `iban` per a la targeta amb identificador `CcU-2938`:

```sql
UPDATE credit_card
SET iban = 'TR323456312213576817699999'
WHERE id = 'CcU-2938';
```

---

## Comprovació del canvi

Per verificar que l’actualització s’ha realitzat correctament, s’ha executat la següent consulta:

```sql
SELECT id, iban
FROM credit_card
WHERE id = 'CcU-2938';
```

El resultat mostra que el nou IBAN s’ha actualitzat correctament.

---

## Conclusions

S’ha modificat correctament el valor del camp `iban` per a la targeta indicada.  
La comprovació posterior confirma que el canvi s’ha aplicat amb èxit a la base de dades.
