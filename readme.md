
<p align="center">
  <img src="puppy.jpg" alt="Pet House GraphQL API" width="250"/>
</p>


# GraphQL Example


### Usage

```sh
$ npm install
```

```sh
$ npm start
```





## Queries & mutations

Let's play with the backend. Go to host URL, in my case; it is `http://localhost:4000/`



```javascript
// get all posts
query{
  posts{
    id
    title
    body
    published
    author{
      
      name
    }
    
  }
}
// get all users
query{
  users{
    id
    name
    email
    age
   comments{
    id
    text
  }
  }
}
// get all comments
query{
  comments{
    id
    text
    author {
      name
    }
  }
}
// create a user
mutation {
  createUser(
    data:{
      name:"amgad",
      email:"amgadhassan28@gmail.com",
      age: 27
    }
    
  ){
    id
    name
    email
    age
  }
}
// create a post
createPost(
    data:{
      title: "my new title",
    body: "",
    published:false,
    author: "b840796d-7534-47da-ace3-a78bfda82a1f" //this the ID of user when you create it 
    }
    
  ){
    id
    title
    body
    published
    author{
      id
      name
    }
    
  }
}

//create an comment 
mutation{
  createComment(
    data:{
      text: "my new title 2",
    author: "3",
    post: "12"
    }
    
    
  ){
    id
    text
    author{
      name
    }
    post{
      title
    }

//Delete a user
mutation{
  deleteUser(id: "1"){
    id
    
  }
}


//and so on you ,,you can find operations that you do them with this project on right side (just click on SCHEMA)


```

