# Graphql queries used:
query getResturant($id: Int = 2) {
  restaurant(id: $id) {
    id
    name
  }
}

query getResturants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

mutation setResturant {
  setrestaurant(input: {name: "Revival House", description: "DJ Rob's house"}) {
    name
    description
  }
}

mutation deleteResturant($id: Int = 1) {
  deleterestaurant(id: $id) {
    ok
  }
}

mutation editrestaurants($idd: Int = 0, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

# Install older version of node
nvm install 14.19.2

# See installed versions
nvm ls

# Use a specific version in current shell
nvm use 14.19.2

# Set a specific version as default
nvm alias default 14.19.2

## Install GraphQL
mkdir graphql
cd graphql
npm init

 # See details here
https://graphql.org/graphql-js/running-an-express-graphql-server/


# Install packages 
npm install


# Or watch changes to code
nodemon index.js
