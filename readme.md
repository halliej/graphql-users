# GraphQL Users Application

The Users application from the "GraphQL with React" course on Udemy.com.

# Sample Queries

{
  user(id: "23") {
    id,
    firstName,
    age
  }
}

{
  user(id: "40") {
    id
    firstName
    age
    company {
      id
      name
      description
    }
  }
}

{
  company(id: "2") {
    id
    name
    description
    users {
      id
      firstName
      age
    }
  }
}
