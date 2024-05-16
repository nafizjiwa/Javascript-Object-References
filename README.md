
# Object-References<br>
------
OBJECTS are data structures used as containers and they store data and functionality. <br>
 - The functionality is stored in methods on our objects. <br>

There are three ways of creating an object in javascript.<br>
  1. Using Object literals <br>
  2. Using the new keyword. <br>
  3. By defining an object constructor and then creating an object constructor type. <br>

<br>
Object Literal: <br>
 
`Their form is key-value pairs.` <br>
`Each key is a string and,` <br>
`Each value is a valid JavaScript data type.` <br>
 <br>
#### SYNTAX:
>let objectName = { <br>
>>this object is assigned to a variable named: objectName <br>
>>object literals are surrounded by curly braces { }<br>
>>they contain --> key: value pairs <br>
>>the keys are like variable names they point to a location holding the value <br>
>>keys are also called ***Identifiers***
>>>>} <br>
###### Example:<br>
    let objectName = {
        'Property Name': 'Property Value',
         propName: 'Prop Value'
    };
<br>

    const person = {
          name: 'John Doe',
          age: 30,
          address: '123 Main Street',
          greet: function() {
                console.log('Hello, my name is ' + this.name);
          }
    }; 
<br>
***Properties*** are what an object HAS and a ***Methods*** are what an object DOES.<br>
<br>
###### Two ways to access an Object key's value:<br>
<br>
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
### Objects are Passed by Reference

Passed by reference means when the object assigned as a variable and passed to a function the parameter is a reference to the memory location of the object. The function will mutate the object not a copy of the object but a function can't reassign the variable assigned to the object.
See Below how to mutate an object through functions.

    let functionName = objectParam => {
      objectParam['Property Name'] = 'New Property Value';                  //This function mutates this 
    };                                                                        //'Property Name' to a 'New Property Value
<br>

    let functionName = objectParam => {
      objectParam.propertyName = 'A Property Value';                      //This function will reassign or set 
    };                                                                     //the propertyName to the assigned value


### Looping Through Objects<br>
We can iterate through objects using the For...in.<br>
for...in will execute a given block of code for EACH PROPERTY IN AN OBJECT.<br>

    for (let variableName in outerObject.innerObject) {
      console.log(`${variableName}: ${outerObject.innerObject[variableName].propertyName}`)
    };
<br>
    
    for (let variableName in outerObject.innerObject) {
      console.log(`${outerObject.innerObject[variableName].propertyName}: 
          ${outerObject.innerObject[variableName].differentPropertyName}`)
    };











