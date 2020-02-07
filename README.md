# pythonREST
### Simple REST Api in Python and MongoDb, deployed on Heroku

Created for study to learn Python and get fun.
You can register a user with email and password, then authenticate and get Bearer Token for make CRUD operations.

I'm like to use Insomnia.
Insomnia is a Cross-platform HTTP and GraphQL Client.

The basic usage is:

Base url for make HTTP requests: https://leberapipython.herokuapp.com

### End-points:

**REGISTER**(method:POST): '/signup'

```json
Body:
{
    "email": "teste@teste.com",
    "password": "123abc"
}
```
**ps**: password must be 6 character lenght minimum

**LOGIN**(method:POST): '/login'

```json
Body:
{
    "email": "teste@teste.com",
    "password": "123abc"
}
Response:
{
  "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpYXQiOjE1ODEwMzY2MjcsIm5iZiI6MTU4MTAzNjYyNywianRpIjoiMTIzZGE5YTgtYmZkMy00ZjkyLTk2NjQtNDc4ODJmNDk1NWNkIiwiZXhwIjoxNTgzNjI4NjI3LCJpZGVudGl0eSI6IjVlM2NhNzFlZjM2NWVjNGViZWU2NjdhOSIsImZyZXNoIjpmYWxzZSwidHlwZSI6ImFjY2VzcyJ9.MFhqaVkOog1nq-6Fp3QIgT4J1UedPklmAtrdfLeWma4"
}
```

**LIST MOVIES**(method:GET): '/movies'

```json
Response:
[
  {
    "_id": {
      "$oid": "5e3cb5354e3ca4c52b16271c"
    },
    "name": "The Dark Knight10",
    "casts": [
      "Christian Bale",
      "Heath Ledger",
      "Aaron Eckhart",
      "Michael Caine"
    ],
    "genres": [
      "Action",
      "Crime",
      "Drama"
    ],
    "added_by": {
      "$oid": "5e3ca71ef365ec4ebee667a9"
    }
  }
]
```

**CREATE**(method:POST): '/movies'

```json
Body:
{
    "name": "Film Name",
    "casts": ["Christian Bale", "Aaron Eckhart"],
    "genres": ["Action", "Crime", "Drama"],
    "added_by": { "$oid": "5e3ca71ef365ec4ebee667a9" }
}

Response:
{
  "id": "5e3cbed4e8a6d4551a13111b"
}
```

**DELETE**(method:DEL): '/movies/<id>' (use the item id)

```json
Body:
{
    "name": "Film Name",
    "casts": ["Christian Bale", "Aaron Eckhart"],
    "genres": ["Action", "Crime", "Drama"],
    "added_by": { "$oid": "5e3ca71ef365ec4ebee667a9" }
}

Response:
{
  "id": "5e3cbed4e8a6d4551a13111b"
}
```

**UPDATE**(method:PUT): '/movies/<id>' (use the item id)

```json
Body: (make the changes)
{
    "name": "Film Name",
    "casts": ["Christian Bale", "Aaron Eckhart"],
    "genres": ["Action", "Crime", "Drama"],
}
```

#### TODOS
- [ ] email confirmation
- [ ] reset password
