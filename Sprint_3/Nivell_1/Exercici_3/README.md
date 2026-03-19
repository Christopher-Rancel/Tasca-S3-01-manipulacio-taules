# Exercici 3 - Inserció d'una nova transacció

## En la taula `transaction` ingressa una nova transacció amb la informació proporcionada.

## Descripció
En aquest exercici he inserit una nova transacció a la taula `transaction` amb les dades indicades a l’enunciat.

Abans d’inserir la transacció, he creat també els registres necessaris a les taules `credit_card` i `company`, ja que els valors `CcU-9999` i `b-9999` no existien i eren necessaris per complir la relació entre taules.

---

## Inserció de dades

Primer s’han afegit els registres necessaris a les taules relacionades:

```sql
INSERT INTO credit_card (id)
VALUES ('CcU-9999');

INSERT INTO company (id)
VALUES ('b-9999');
```

Després s’ha inserit la nova transacció:

```sql
INSERT INTO `transaction` (
    id,
    credit_card_id,
    company_id,
    user_id,
    lat,
    longitude,
    amount,
    declined
)
VALUES (
    '108B1D1D-5B23-A76C-55EF-C568E49A99DD',
    'CcU-9999',
    'b-9999',
    9999,
    829.999,
    -117.999,
    111.11,
    0
);
```

---

## Comprovació

Per comprovar que la inserció s’ha realitzat correctament, he executat la següent consulta:

```sql
SELECT *
FROM `transaction`
WHERE id = '108B1D1D-5B23-A76C-55EF-C568E49A99DD';
```

El resultat mostra que la nova transacció s’ha guardat correctament a la base de dades.

---

## Conclusions

S’ha inserit correctament una nova transacció a la taula `transaction`.  
També s’han creat prèviament els registres necessaris a les taules relacionades per mantenir la integritat referencial de la base de dades.
