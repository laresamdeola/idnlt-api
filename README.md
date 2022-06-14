#### [idnlt-api](https://idnlt-api2.herokuapp.com/infections)

i do not like this(idnlt) is an API containing information about Sexually Transmitted Diseases(STDs).

#### INTRODUCTION 🤟
idnlt arose from the necessity to have an API whereby one can easily fetch the symptoms of different Sexually Transmitted Infections. The API is open and free to use and currently contains a total of 11 common STI's along with their associated symptoms in *men* and *women*.

![idnlt](./idnlt.jpg)

#### OBJECT KEYS 🔑
There are a few other key value pairs apart from symptoms that can be fetched from the idnlt API.

- [x] id
- [x] infectionName
- [x] symptomsWomen
- [x] symptomsMen
- [x] nickName
- [x] isThereVaccine

#### SAMPLE 📙 

Here's a brief code snippet, using Node.js as the backend with the fetch API to fetch data from the idnlt API: 

```
***import the dependencies***

import fetch from 'node-fetch'
import express from "express"

const app = express()

const idnlt = "https://idnlt-api2.herokuapp.com/infections"

***the aysnc function to fetch the data from the api***

const fetchData = async (url) => {
  try{
    let response = await fetch(url)
    let data = await response.json()
    console.log(data)
  } catch(error){
    console.log(error.message)
  }
}

***the get route***

app.get('/', (req, res) => {
  const displayData = fetchData(idnlt)
  console.log(displayData)
})

app.listen(3000, () => {
  console.log("Server ti wa online")
})
```

#### TECHNOLOGIES 🔨

- [x] HTML5
- [x] CSS3
- [x] JAVASCRIPT
- [x] NODEJS
- [x] EXPRESS.JS
- [x] DOCKER
- [x] HEROKU



