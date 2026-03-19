# Nivell 2 - Exercici 3

## Filtrat de la vista VistaMarketing

## Descripció
En aquest exercici s’ha utilitzat la vista `VistaMarketing` per obtenir informació específica de les companyies.

S’ha filtrat la informació per mostrar només aquelles empreses que tenen com a país de residència "Germany".

---

## Consulta

```sql
SELECT *
FROM VistaMarketing
WHERE country = 'Germany';
```

---

## Resultat

El resultat mostra únicament les companyies amb país "Germany", juntament amb el seu telèfon i la mitjana de compra.

---

## Conclusions

S’ha aplicat correctament un filtre sobre una vista ja creada, demostrant la utilitat de les vistes per simplificar consultes i facilitar l’anàlisi de dades.
