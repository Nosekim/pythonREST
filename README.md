# pythonREST
### Simple REST Api in Python with Flask, deployed on Heroku

Created for study to learn Python and get fun.
You can register a user with email and password, then authenticate and get Bearer Token for make CRUD operations.

I'm like to use Insomnia.
Insomnia is a Cross-platform HTTP and GraphQL Client.

The basic usage is:

Base url for make HTTP requests: https://leberapipython.herokuapp.com

### End-points:

REGISTER: '/signup'

Body:
```json
{
    "email": "teste@teste.com",
    "password": "123abc"
}
```
ps: password must be 6 character lenght minimum

LOGIN: '/login'

Body:
```json
{
    "email": "teste@teste.com",
    "password": "123abc"
}
```


#### TODOS
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
