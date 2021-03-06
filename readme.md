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
  users {
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

{
  apple: company(id: "1") {
    id
    name
    description
    users {
      id
      firstName
      age
    }
  }
  google: company(id: "1") {
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

{
  apple: company(id: "1") {
    ...companyDetails
    users {
      id
      firstName
      age
    }
  }
  google: company(id: "1") {
    ...companyDetails
    users {
      id
      firstName
      age
    }
  }
}

fragment companyDetails on Company {
  id
  name
  description
}

mutation {
  addUser (
    firstName: "Stephen", age: 26) {
    	id
    	firstName
    	age
  	}
}

mutation {
  deleteUser(id: "23") {
    id
  }
}

mutation {
 	editUser(id: "41", firstName: "Bob") {
  	id
    firstName
    age
	}
}
