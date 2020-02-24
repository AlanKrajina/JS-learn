#### Create server.js

```js
// backend API

const express = require('express');

const app = express();


// route and json data
app.get('/api/boxers', (req, res) => {
  const boxers = [
    {id: 1, firstName: 'Anthony', lastName: 'Joshua'},
    {id: 2, firstName: 'Tyson', lastName: 'Fury'},
    {id: 3, firstName: 'Deontay', lastName: 'Wilder'},
  ];

  res.json(boxers);
});


// port configuration
const port = 5000;

app.listen(port, () => `Server running on port ${port}`);
```

#### Get data from server

```js
import React, { useState, useEffect } from 'react';
import './boxers.css';


const Boxers = () => {

  const [boxers,setBoxers] = useState([])

  useEffect(() => {
    fetch('/api/boxers')
      .then(res => res.json())
      .then(boxersAll => setBoxers(boxersAll));
    }, []);


  return (
    <div>
    <h2>Boxers</h2>
    <ul>
      {boxers.map(boxer => 
        <li key={boxer.id}>{boxer.firstName} {boxer.lastName}</li>
      )}
    </ul>
  </div>    
  )
}

export default Boxers;
```
