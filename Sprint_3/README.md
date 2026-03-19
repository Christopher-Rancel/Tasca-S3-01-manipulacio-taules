# Sprint 3 – Manipulació de Taules SQL

# Descripció

En aquest sprint es treballa la manipulació de taules en bases de dades relacionals mitjançant MySQL.  
L’objectiu és aplicar operacions sobre l’estructura i les dades d’una base de dades que conté informació d’una empresa amb transaccions, empreses, targetes de crèdit i usuaris.

Durant aquest sprint es realitzen tasques com la creació i modificació de taules, la inserció i eliminació de dades, la gestió de relacions entre taules i la creació de vistes per facilitar l’anàlisi de la informació.

---

## Nivell_1

### Exercici_1
Creació de la base de dades i importació de les taules `company` i `transaction`.  
Anàlisi de l’estructura de les taules i generació del diagrama EER per visualitzar les relacions.

### Exercici_2
Actualització d’un registre incorrecte a la taula `credit_card`, modificant el número de compte associat a una targeta de crèdit.

### Exercici_3
Inserció d’una nova transacció a la taula `transaction`, assegurant la coherència amb les claus foranes i la integritat de les dades.

### Exercici_4
Modificació de l’estructura de la taula `credit_card` mitjançant l’eliminació de la columna `pan`.

---

## Nivell_2

### Exercici_1
Eliminació d’un registre concret de la taula `transaction` utilitzant una clàusula `WHERE` per garantir que només s’elimini el registre indicat.

### Exercici_2
Creació de la vista `VistaMarketing`, que permet analitzar la informació de les empreses:

- Nom de la companyia  
- Telèfon  
- País  
- Mitjana de compra  

Els resultats es mostren ordenats de major a menor mitjana.

### Exercici_3
Filtrat de la vista `VistaMarketing` per mostrar únicament les empreses amb país `"Germany"`.

---

## Nivell_3

### Exercici_1
Adaptació del model de dades per coincidir amb el diagrama EER proporcionat:

- Creació de la taula `user`
- Inserció de dades dels usuaris
- Modificació del tipus de dada de la clau primària (`id`)
- Inserció del registre necessari (`user_id = 9999`)
- Creació de la relació entre `transaction` i `user`
- Modificació de la taula `credit_card` afegint la columna `fecha_actual`
- Comprovació final de l’estructura i les relacions

### Exercici_2
Creació de la vista `InformeTecnico`, que integra informació de diverses taules:

- ID de la transacció  
- Nom i cognom de l’usuari  
- IBAN de la targeta de crèdit  
- Nom de la companyia  

La vista es construeix mitjançant múltiples `JOIN` i es mostra ordenada de forma descendent segons l’ID de la transacció.

---

## Objectiu del Sprint

L’objectiu d’aquest sprint és consolidar els coneixements sobre manipulació de dades i estructures en SQL, incloent:

- Creació i modificació de taules (`CREATE`, `ALTER`, `DROP`)
- Inserció i eliminació de dades (`INSERT`, `DELETE`)
- Gestió de claus foranes i integritat referencial
- Creació i ús de vistes (`CREATE VIEW`)
- Consultes amb múltiples `JOIN`
- Organització i verificació de l’estructura de la base de dades

Aquest sprint forma part del procés d’aprenentatge en anàlisi de dades i bases de dades relacionals.
