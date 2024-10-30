# Demo Project for Spring Boot

## Descrizione
Questo è un progetto demo che utilizza Spring Boot per creare un'applicazione RESTful con MongoDB e Redis. L'applicazione gestisce prodotti, permettendo operazioni CRUD (Create, Read, Update, Delete) e caching con Redis.

## Requisiti
- Java 17
- Maven
- MongoDB
- Redis

## Struttura del Progetto
- `src/main/java/com/example/demo/controller`: Contiene i controller REST.
- `src/main/java/com/example/demo/service`: Contiene i servizi di business logic.
- `src/main/java/com/example/demo/repository`: Contiene i repository per l'accesso ai dati.
- `src/main/java/com/example/demo/domain`: Contiene le entità di dominio.
- `src/main/java/com/example/demo/redis`: Contiene la configurazione di Redis.

## Configurazione
### `pom.xml`
Il file `pom.xml` include le dipendenze per Spring Boot, MongoDB, Redis e Lombok.

### `RedisConfig.java`
Configura il `CacheManager` e il `RedisTemplate` per l'uso di Redis come cache.

## Esecuzione del Progetto
1. Clonare il repository.
2. Configurare MongoDB e Redis.
3. Eseguire il comando `mvn spring-boot:run` per avviare l'applicazione.

## API Endpoints
### ProductController
- **GET /products**: Recupera tutti i prodotti.
- **GET /products/{id}**: Recupera un prodotto per ID.
- **POST /products**: Crea un nuovo prodotto.
- **PUT /products/{id}**: Aggiorna un prodotto esistente.
- **DELETE /products/{id}**: Elimina un prodotto per ID.

## Caching
Il caching è configurato per i metodi di `ProductService` utilizzando le annotazioni `@Cacheable`, `@CachePut` e `@CacheEvict`.
