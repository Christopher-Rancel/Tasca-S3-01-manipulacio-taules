# Nivell 2 - Exercici 1

## Eliminació d'un registre

## Descripció
En aquest exercici s’ha eliminat un registre concret de la taula `transaction` a partir del seu identificador.

---

## Comprovació prèvia

Primer s’ha verificat que el registre existia:

```sql
SELECT *
FROM `transaction`
WHERE id = '000447FE-B650-4DCF-85DE-C7ED0EE1CAAD';
```

---

## Eliminació del registre

S’ha utilitzat la següent instrucció:

```sql
DELETE FROM `transaction`
WHERE id = '000447FE-B650-4DCF-85DE-C7ED0EE1CAAD';
```

---

## Comprovació final

Per assegurar que el registre s’ha eliminat correctament:

```sql
SELECT *
FROM `transaction`
WHERE id = '000447FE-B650-4DCF-85DE-C7ED0EE1CAAD';
```

El resultat mostra que el registre ja no existeix a la base de dades.

---

## Conclusions

S’ha eliminat correctament el registre indicat de la taula `transaction` utilitzant una clàusula WHERE per garantir que només s’elimini el registre desitjat.
