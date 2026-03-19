# Tasca S3.01 - Manipulació de taules

## Descripció

En aquest sprint es treballa la manipulació de taules en bases de dades relacionals utilitzant MySQL.  
L’activitat consisteix en crear, modificar i relacionar diferents taules, així com en la creació de vistes per facilitar l’anàlisi de la informació.

Es treballa sobre una base de dades que conté informació sobre empreses, transaccions, targetes de crèdit i usuaris.

---

## Estructura de la base de dades

El projecte treballa amb les següents taules:

- `company` → informació de les empreses  
- `transaction` → registres de transaccions  
- `credit_card` → informació de targetes de crèdit  
- `user` → informació dels usuaris  

Les taules estan relacionades mitjançant claus primàries i claus foranes:

- `transaction.company_id → company.id`
- `transaction.credit_card_id → credit_card.id`
- `transaction.user_id → user.id`

---

## Nivell 1

### Exercici 1
Creació i importació de les taules `company` i `transaction`, així com anàlisi de la seva estructura.

### Exercici 2
Correcció d’un error en el número de compte associat a una targeta de crèdit.

### Exercici 3
Inserció d’una nova transacció a la taula `transaction`, assegurant la coherència amb les claus foranes.

### Exercici 4
Eliminació de la columna `pan` de la taula `credit_card`.

---

## Nivell 2

### Exercici 1
Eliminació d’un registre concret de la taula `transaction` utilitzant una clàusula `WHERE`.

### Exercici 2
Creació de la vista `VistaMarketing`, que mostra:
- Nom de la companyia  
- Telèfon  
- País  
- Mitjana de compra  

Ordenada de major a menor mitjana.

### Exercici 3
Filtrat de la vista `VistaMarketing` per mostrar només les empreses amb país `"Germany"`.

---

## Nivell 3

### Exercici 1
Adaptació del model de dades per coincidir amb el diagrama EER:

- Creació de la taula `user`
- Inserció de dades d’usuaris
- Modificació del tipus de dada de `id` per compatibilitat
- Inserció del registre `user_id = 9999`
- Creació de la relació entre `transaction` i `user`
- Afegir la columna `fecha_actual` a `credit_card`
- Comprovació final de l’estructura i relacions

### Exercici 2
Creació de la vista `InformeTecnico`, que inclou:

- ID de la transacció  
- Nom i cognom de l’usuari  
- IBAN de la targeta de crèdit  
- Nom de la companyia  

Utilitzant `JOIN` entre múltiples taules i ordenant els resultats de forma descendent.

---

## Objectiu del projecte

L’objectiu d’aquesta activitat és consolidar els coneixements sobre manipulació de dades en SQL, incloent:

- Creació i modificació de taules (`CREATE`, `ALTER`, `DROP`)
- Inserció i eliminació de dades (`INSERT`, `DELETE`)
- Gestió de claus foranes i integritat referencial
- Ús de vistes (`CREATE VIEW`)
- Consultes amb múltiples `JOIN`
- Funcions d’agregació (`AVG`, `ROUND`)
- Ordenació i filtratge de dades

Aquest projecte forma part del procés d’aprenentatge en anàlisi de dades i bases de dades relacionals.
