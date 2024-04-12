# Books example application 
(based on the example from Dan Vega: GraphQL Spring Boot - How to get started with Spring for GraphQL https://www.youtube.com/watch?v=3PCNqXrU-2g)

Dependencies:
 - Spring web (`spring-boot-starter-web`) https://docs.spring.io/spring-boot/docs/current/reference/html/web.html 
 - Spring for GraphQL (`spring-boot-starter-graphql` ) https://spring.io/projects/spring-graphql

# Run the app
`./gradlew bootRun`

# Open GraphiQL web tool (see: https://github.com/graphql/graphiql)

http://localhost:8080/graphiql

# Query books

```
query {
  allBooks {
    id
    title,
    author {
      firstName,
      lastName
    }
  }
}
```

Response:
```
{
  "data": {
    "allBooks": [
      {
        "id": "1",
        "title": "Reactive Spring",
        "author": {
          "firstName": "Josh",
          "lastName": "Long"
        }
      },
      {
        "id": "2",
        "title": "Spring Boot Up & Running",
        "author": {
          "firstName": "Mark",
          "lastName": "Heckler"
        }
      },
      {
        "id": "3",
        "title": "Hacking with Spring Boot 2.3",
        "author": {
          "firstName": "Greg",
          "lastName": "Turnquist"
        }
      }
    ]
  }
}`
```
