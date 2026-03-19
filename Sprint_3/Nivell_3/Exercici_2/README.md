# Exercici 2 – Nivell 3

## Descripció

En aquest exercici s’ha creat una vista anomenada `InformeTecnico` per agrupar informació rellevant de diferents taules de la base de dades en una sola consulta.

Aquesta vista mostra l’identificador de la transacció, el nom i cognom de l’usuari/ària, l’IBAN de la targeta de crèdit utilitzada i el nom de la companyia associada a la transacció.

---

## Pas a pas

### 1. Creació de la vista

S’ha creat la vista `InformeTecnico` utilitzant dades de les taules `transaction`, `user`, `credit_card` i `company`.

```sql
CREATE VIEW InformeTecnico AS
SELECT
    t.id AS transaction_id,
    u.name AS user_name,
    u.surname AS user_surname,
    ccard.iban AS credit_card_iban,
    c.company_name AS company_name
FROM `transaction` t
JOIN user u
    ON t.user_id = u.id
JOIN credit_card ccard
    ON t.credit_card_id = ccard.id
JOIN company c
    ON t.company_id = c.id;
```

---

### 2. Consulta de la vista

Per visualitzar la informació de la vista, s’ha executat la consulta següent:

```sql
SELECT *
FROM InformeTecnico
ORDER BY transaction_id DESC;
```

---

## Conclusió

S’ha creat correctament una vista que permet consultar de manera senzilla informació tècnica rellevant sobre les transaccions, els usuaris, les targetes de crèdit i les companyies.
