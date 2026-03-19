# Nivell 1 - Exercici 1

## Crea una taula anomenada `credit_card` que permeti emmagatzemar els detalls de les targetes de crèdit. Estableix una relació amb la taula `transaction` i mostra el diagrama EER resultant, tot fent una breu descripció.

## Descripció
En aquest exercici he creat una nova taula anomenada `credit_card` dins la base de dades `transactions`.  
L’objectiu és guardar la informació de les targetes de crèdit i relacionar-les amb les transaccions ja existents.

---

## Estructura de la base de dades

### Taula `credit_card`

Aquesta taula guarda la informació de les targetes de crèdit:

- `id` → Identificador únic de la targeta (clau primària)
- `iban` → Codi IBAN associat a la targeta
- `pan` → Número de la targeta
- `pin` → Codi PIN de la targeta
- `cvv` → Codi CVV de la targeta
- `expiring_date` → Data de caducitat de la targeta

---

## Inserció de dades

Després de crear la taula, s’han introduït les dades del document `dades_introduir_credit`.

Per comprovar que les dades s’han carregat correctament, he executat la següent consulta:

```sql
SELECT COUNT(*) AS total_registres
FROM credit_card;
```

El resultat obtingut ha estat de **5000 registres**.

---

## Relació entre les taules

La taula `credit_card` es relaciona amb la taula `transaction` mitjançant el camp `credit_card_id`.

Això permet que cada transacció quedi associada a una targeta de crèdit concreta.

També es manté la relació entre `transaction` i `company`, on cada transacció pertany a una empresa.

Per tant, la taula `transaction` actua com a taula central dins del model.

---

## Diagrama EER

El diagrama EER mostra com es relacionen les taules `company`, `transaction` i `credit_card`.

La taula `transaction` està relacionada amb `company` a través del camp `company_id` i amb `credit_card` a través del camp `credit_card_id`.  
Això permet saber quina empresa i quina targeta estan associades a cada transacció.

---

## Codi

```sql
DESCRIBE credit_card;

SELECT COUNT(*) AS total_registres
FROM credit_card;

SELECT t.id, t.credit_card_id, c.id
FROM `transaction` t
JOIN credit_card c
    ON t.credit_card_id = c.id
LIMIT 10;
```
