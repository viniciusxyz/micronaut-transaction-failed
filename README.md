## Micronaut 3.3.0 Documentation

- [User Guide](https://docs.micronaut.io/3.3.0/guide/index.html)
- [API Reference](https://docs.micronaut.io/3.3.0/api/index.html)
- [Configuration Reference](https://docs.micronaut.io/3.3.0/guide/configurationreference.html)
- [Micronaut Guides](https://guides.micronaut.io/index.html)
---

## Feature http-client documentation

- [Micronaut HTTP Client documentation](https://docs.micronaut.io/latest/guide/index.html#httpClient)

## Post for test:

**With exception**

```bash
curl --location --request POST 'http://localhost:8080/deposit/throw' \
--header 'Content-Type: application/json' \
--data-raw '{
"accountNumber": "0000001",
"amount": 1.0
}'
```

**Without exception**

```bash
curl --location --request POST 'http://localhost:8080/deposit' \
--header 'Content-Type: application/json' \
--data-raw '{
"accountNumber": "0000001",
"amount": 1.0
}'
```

### H2 Console

http://localhost:8082

- jdbc:h2:mem:testdb;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE
- sa
- password

**Selects for test**

```sql
select * from accounts;
select * from deposit_history;
```