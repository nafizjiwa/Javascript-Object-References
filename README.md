# Object-References<br>
------
Object Literal: <br>

let objectName = { <br>
    this object is assigned to a variable named: objectName <br>
    object literals are surrounded by curly braces { }<br>
    they contain --> key: value pairs <br>
    the keys are like variable names they point to a location holding the value <br>
    keys are also called ***Identifiers***
} <br>

    let objectName = {
    'Property Name': 'Property Value',
     propName: 'Prop Value'
    };
  
Methods are data stored in an object as a function<br>
***Properties*** are what an object HAS and a ***Methods*** are what an object DOES.<br>
Methods in our object literals by creating ordinary, colon-separated key-value pairs. The key serves as our method’s name, while the value is an anonymous function expression.<br>

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
    };
    
`spaceship['Active Duty'];   // Returns true`<br>
`spaceship['Fuel Type'];   // Returns  'Turbo Fuel'`<br>
`spaceship['numCrew'];   // Returns '5'`<br>
`spaceship.numCrew;   // Returns  '5'`<br>
`spaceship.homePlanet; // Returns 'Earth'`<br>
`spaceship.color; // Returns 'silver'`<br>
`spaceship.favoriteIcecream; // Returns undefined`<br>
Above object property favoriteIcecream is not in the spaceship object above hence this property can not be found<br>


