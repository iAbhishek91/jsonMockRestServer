# jsonMockRestServer
Rest mock server returning JSON

### module used
refer: (json-server documentation)[https://www.npmjs.com/package/json-server]

### access in-house json
`yarn run json:server`

### access remote json
`yarn run json:server:remote`
### default directory
`./public`

#### resources
they are object available in JSON
- http://localhost:3000/employee
- http://localhost:3000/employer
- http://localhost:3000/db the entire object

#### get single company
- http://localhost:3000/employer/1

#### get all employee of a particular employer (create a relation)
- http://localhost:3000/employer/1/employee

also see about _expand and _embed
#### filter companies by name
- http://localhost:3000/employer?name=Royel%20Dutch%20Shell

#### pagination and Limit
- http://localhost:3000/employer?_page=1&_limit=2

by default returns 10 data, if limit is not used

#### sorting and sorting order
- http://localhost:3000/employer?_sort=name&_order=asc

#### age range
- http://localhost:3000/employee?age_gte=40&age_lte=55

- other operators:
_gte, _lte, _ne, _like(regex supported)

### slice
- _start=20&_end=30&_limit=10
#### search by string
- http://localhost:3000/employee?q=george