# Exercici 1 – Nivell 3

## Descripció

En aquest exercici s’ha adaptat l’estructura de la base de dades per tal que coincideixi amb el diagrama EER proporcionat. S’ha treballat amb les taules existents i s’ha afegit la informació dels usuaris, així com les relacions necessàries entre taules.

---

## Pas a pas

### 1. Creació de la taula d’usuaris

S’ha creat la taula `user` per emmagatzemar la informació dels usuaris:

```sql
CREATE TABLE user (
    id CHAR(10) PRIMARY KEY,
    name VARCHAR(100),
    surname VARCHAR(100),
    phone VARCHAR(150),
    email VARCHAR(150),
    birth_date VARCHAR(100),
    country VARCHAR(150),
    city VARCHAR(150),
    postal_code VARCHAR(100),
    address VARCHAR(255)
);
```

---

### 2. Inserció de dades

S’han inserit les dades dels usuaris utilitzant el fitxer proporcionat:

```sql
INSERT INTO user (id, name, surname, phone, email, birth_date, country, city, postal_code, address)
VALUES (...);
```

---

### 3. Comprovació de les dades

```sql
SELECT COUNT(*) AS total_users
FROM user;
```

---

### 4. Adaptació del tipus de dada

S’ha detectat un error en crear la relació amb la taula `transaction`, ja que els camps no tenien el mateix tipus de dada.  
Per solucionar-ho, s’ha modificat el camp `id`:

```sql
ALTER TABLE user
MODIFY COLUMN id INT;
```

---

### 5. Inserció del registre que faltava

S’ha detectat que el valor `user_id = 9999` existia a la taula `transaction` però no a la taula `user`, així que s’ha inserit manualment:

```sql
INSERT INTO user (id)
VALUES (9999);
```

---

### 6. Creació de la relació entre taules

```sql
ALTER TABLE `transaction`
ADD CONSTRAINT fk_transaction_user
FOREIGN KEY (user_id) REFERENCES user(id);
```

---

### 7. Comprovació de la relació

```sql
SELECT t.id, t.user_id, u.id, u.name, u.surname
FROM `transaction` t
JOIN user u
    ON t.user_id = u.id
LIMIT 10;
```

---

### 8. Modificació de la taula credit_card

Per adaptar-la al diagrama, s’ha afegit la columna `fecha_actual`:

```sql
ALTER TABLE credit_card
ADD COLUMN fecha_actual DATE;
```

---

### 9. Comprovació final

```sql
DESCRIBE company;
DESCRIBE user;
DESCRIBE credit_card;
DESCRIBE `transaction`;
```

---

## Diagrama EER

Finalment, s’ha generat el diagrama EER per comprovar que l’estructura de la base de dades coincideix amb el model proporcionat.

---

## Conclusió

S’ha aconseguit adaptar correctament la base de dades al model indicat, creant la taula d’usuaris, afegint les dades, solucionant errors de tipus de dades i establint les relacions entre les taules.
