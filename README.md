# Apollo Space Camp Demo Code

**Installation:**

```sh
npm i && npm run server
```

**Code Along:**

[Watch the recording of the talk here](https://www.youtube.com/watch?v=zZnHA3yyPJY&t=1987s) 👩‍💻


**Background:**

```sh
type Astronaut {
  id: ID!
  name: String
  missions: [Mission]
}
type Mission {
  id: ID!
  designation: String!
  startDate: String
  endDate: String
}
```

```sh
query allAstronautNames {
  astronaut {
    id  
    name
  }
}
```
```sh
query allAstronautNamesAndMissions {
  astronaut {
    id
    name
    missions {
      id  
      designation
    }
    }

}
```
```sh
"Astronaut": [
  {
    "id": "123"
    "name": "Neil Armstrong"
    "missions": [{
      "id": "m1"  
      designation: "Chief"
    }, {
      "id": "m2"  
      designation: "Assistant"
    }]
  },
  {
    "id": "789"
    "name": "Buzz Aldrin"
    "missions": [{
      "id": "m2"  
      designation: "Assistant"
    }, {
      "id": "m3"  
      designation: "Assistant"
    }]
  }
]
```
```sh
query myAstronaut {
  astronaut(id: "789") {
    id  
    name
  }
}
```


