# Read: Class 01

## Review, Research, and Discussion

1. A Map object iterates its elements in insertion order - a for...of loop returns an array of [key, value] for each iteration.

2. executes a reducer function (that you provide) on each element of the array, resulting in single output value.

3. Provide code snippets showing how to use superagent() to fetch data from a URL and log the result
    - With normal Promise .then() syntax

          function getCharacters(){
          superagent.get('https://swapi.dev/api/people')
          .then(data=>{
            // console.log(data.body.results);
              let charObj = {};
              let name = data.body.results[3].name;
              let url = data.body.results[3].url;
              charObj[name] = url;
              
              console.log(JSON.stringify(charObj));
            })
          .catch(err => console.log(err))
          }
          getCharacters();

    - Again with async / await syntax
          
          async function cityData(cityName){

            let url = `https://geocode.xyz/${cityName}?json=1`;

            superagent.get(url)
              .then(data =>{
                // console.log(data.body);
                console.log(`${cityName.toUpperCase()}: Longitude is ${data.body.longt}, Latitude is ${data.body.latt}`);
              })
          }

          cityData('Mata Obscura');


4. Explain promises as though you were mentoring a Code 301 level student

    - the asynchronous method returns a promise to supply the value at some point in the future. **Here is a reference [promise MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)**

5. Are all callback functions considered to be Asynchronous? Why or Why Not?

    - No, **asynchronous callbacks** are put on the task queue to finish the currently executing tasks first & then once the execution stack is empty, event loop will pick the waiting tasks for execution.
    - **Synchronous callbacks** can return to the caller immediately after it's invoked ***such as forEach, map, filter***