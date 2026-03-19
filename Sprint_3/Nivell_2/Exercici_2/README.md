# Nivell 2 - Exercici 2


## Descripció
En aquest exercici s’ha creat una vista anomenada `VistaMarketing` per proporcionar informació rellevant sobre les companyies i les seves transaccions.

L’objectiu és facilitar l’anàlisi de dades per part del departament de màrqueting.

---

## Creació de la vista

S’ha utilitzat la següent instrucció SQL:

```sql
CREATE VIEW VistaMarketing AS
SELECT 
    c.company_name,
    c.phone,
    c.country,
    ROUND(AVG(t.amount), 2) AS avg_purchase
FROM company c
JOIN `transaction` t 
    ON c.id = t.company_id
WHERE t.declined = 0
GROUP BY 
    c.company_name,
    c.phone,
    c.country
ORDER BY avg_purchase DESC;
```

---

## Comprovació

Per visualitzar la vista creada:

```sql
SELECT *
FROM VistaMarketing;
```

El resultat mostra les companyies amb la seva informació i la mitjana de compra, ordenades de major a menor.

---

## Conclusions

S’ha creat correctament una vista que permet analitzar el comportament de compra de les empreses. Aquesta informació pot ser útil per a estratègies de màrqueting i presa de decisions.
