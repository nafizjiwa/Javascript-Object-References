# Object-References<br>
------
Object Literal: <br>

>let objectName = { <br>
>>this object is assigned to a variable named: objectName <br>
>>object literals are surrounded by curly braces { }<br>
>>they contain --> key: value pairs <br>
>>the keys are like variable names they point to a location holding the value <br>
>>keys are also called ***Identifiers***
>>>>} <br>
###### Example:
    let objectName = {
    'Property Name': 'Property Value',
     propName: 'Prop Value'
    };
  
***Properties*** are what an object HAS and a ***Methods*** are what an object DOES.<br>
###### Two ways to access an Object key's value:<br>
1. Dot notation<br>
   
       const variableName = objectName.propertyName;
2. Bracket notation<br>

       let variableName = objectName['propertyName'];
 

If we try to access a property that does not exist on that object, undefined will be returned.<br>

       objectName.propertyName(name which is not the in object);// Returns undefined

Example:<>br

    let spaceship = {
      'Fuel Type': 'Turbo Fuel',
      'Active Duty': true,
      homePlanet: 'Earth',
      numCrew: 5
      homePlanet: 'Earth',
      color: 'silver'
      invade: function () { 
            console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
          }
    };
    
`spaceship['Active Duty'];               // Returns true`<br>
`spaceship['Fuel Type'];                   // Returns  'Turbo Fuel'`<br>
`spaceship['numCrew'];                      // Returns '5'`<br>
`spaceship.numCrew;                          // Returns  '5'`<br>
`spaceship.color;                              // Returns 'silver'`<br>
`spaceship.favoriteIcecream;                    // Returns undefined`<br>
<br>
Above object property favoriteIcecream is not in the spaceship object above hence this property can not be found, so returns undefined<br>

***Bracket Notation allows us to use variables inside brackets to select keys of an object***<br>

    let returnAnyProp = (objectName, propName) =>                                  // propName is a variable and
                            objectName[propName];                               // the function looks for the variables value
        console.log(returnAnyProp(spaceship, 'homePlanet'));                                 // Returns 'Earth'

Methods are data stored in an object as a function<br>
Using methods in an object literals:  key-value pairs. The key serves as our method’s name, while the value is an anonymous function expression.<br>

    const variableName = {
          methodsName: valueIsFunction () { 
                console.log('This is a method which can be involked or called.')
              }
    };
ES6 allows a new syntax for methods in object literals where we can ***omit*** the ***__colon__*** and the ***__function keyword___***.

    const variableName = {
          methodsName () { 
                console.log('This method has no colon or keyword function so recognize the syntax when in an object literal.')
              }
    };
     const alienShip = {
          invade () { 
                console.log('INVOKE THIS METHOD LIKE SO: alienShip.invade(); .')
              }
    };












