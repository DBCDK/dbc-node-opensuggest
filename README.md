# dbc-node-opensuggest
Client for the DBC OpenSuggestion service

Implements the suggest method that based on query parameters gives suggestions
for continued search.

## Example
```
import OpenSuggest from 'dbc-node-opensuggest'

// Setup service 
const endpoint = 'http://opensuggestion.addi.dk/';
let openSuggest = OpenSuggest(endpoint);

// Setup data
const params = {
  index: 'scanphrase.creator',
  query: 'Karl'
};

// Make response
openSuggest.getSuggestions(params)
  .then((reponse) => {
    // Everything went well
    console.log(reponse);
  })
  .catch((reponse) => {
    // Something went wrong
    console.log(reponse);
  });

};
```

Calls to a method on the client returns a Promise object