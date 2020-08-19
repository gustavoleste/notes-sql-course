# INSERT COMMAND

## EXAMPLES:
```bash
INSERT INTO <table-name>
(<colunm-1>,<colunm-2>,...)
VALUES
(<value-1>,<value-2>,...);
```
```sql
INSERT INTO chitter_user
(user_id,username,encrypted_password,email,date_joined)
VALUES
(DEFAULT, 'firstuser','4d4d4df7f4','firstuser@email.com','2020-08-17');
```
```sql
INSERT INTO chitter_post
(user_id,post_text)
VALUES
(1,'Hello World!'),
(2,'Hello Solar System!');
```