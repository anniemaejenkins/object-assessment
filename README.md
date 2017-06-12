## Scope, hoisting and compartmentalization

### Answer the following:
In you own words, explain the concepts of scope, hoisting, compartmentalization.

Scope: There are two scopes, local and global. Local scope refers to the space within a function and the variables inside cannot be accessed from outside the function.
Global scope is everything outside of the functions and can be easily accessed by others so it's advised to not place any variables in the global scope so others aren't able to redefine variables to change things.

Hoisting: Moves variables without their assignments to the top of functions. Best practice would suggest to always declare your variables at the top of a function to avoid any messups.

Compartmentalization: In order to protect information from outsiders, it's necessary to declare variables and sensitive information inside of objects so that they aren't inside the global scope.


### Provide examples for all three, below:

#### Scope:
        <---- global space


function stuff{
var x = personal things
     <--- local space
};


#### Hoisting:


function stuff{

  function otherfunction{
    var y = whatever;
  };
  var x = personal things;
};
/////after calling function///
function stuff {
  var x;         <--- the variable was moved to the top----
  function otherfunction{
    var y = whatever;
  };
  = personal things
};


#### Compartmentalization:

function stuff{
  var x = personal things;
  function otherfunction{
    var y = whatever;  <-----keeping var y out of the global scope----
  };
};
