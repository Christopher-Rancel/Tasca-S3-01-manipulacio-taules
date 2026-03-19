# Exercici 4 - Eliminació d'una columna

## Descripció
En aquest exercici s’ha eliminat la columna `pan` de la taula `credit_card`, tal com s’indica a l’enunciat.

---

## Eliminació de la columna

S’ha utilitzat la següent instrucció SQL:

```sql
ALTER TABLE credit_card
DROP COLUMN pan;
```

---

## Comprovació

Per verificar que la columna s’ha eliminat correctament, s’ha executat:

```sql
DESCRIBE credit_card;
```

El resultat mostra que la columna `pan` ja no existeix dins de la taula.

---

## Conclusions

S’ha modificat correctament l’estructura de la taula `credit_card`, eliminant la columna `pan` segons els requisits de l’exercici.
