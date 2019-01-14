---
title: Use a Switch Statement to Handle Multiple Actions
---
## Use a Switch Statement to Handle Multiple Actions

Tip: Make sure you don't use "break" commands after return statements within the switch cases.

Our solution steps are as following:

* First, we check if the login.type is 'LOGIN' so we edit the state authenticated to TRUE and return the final edition. 

* Second, we check if the login.type is 'LOGOUT' so we edit the state authenticated to FALSE and return the final edition.

* Finally, the default case is to return the current state so anytime a dispatch happens due to any other action which doesn't relate to the reducer, the current state doesn't effect. 


```

const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {
  // change code below this line
  // start the switch statement 
  switch(action.type){
    //if the login type is 'LOGIN' then change the value of the authenticated state to true and return the state 
    case 'LOGIN':
    return {authenticated : true};
    break;

    //if the login type is 'LOGOUT' then change the value of the authenticated state to false and return the state 
    case "LOGOUT":
    return {authenticated : false};
    break;

    //default case is to return the current value of the state
    default:
    return state;
  }

  // change code above this line
};

```

This is a stub. <a href='https://github.com/freecodecamp/guides/tree/master/src/pages/certifications/front-end-libraries/redux/use-a-switch-statement-to-handle-multiple-actions/index.md' target='_blank' rel='nofollow'>Help our community expand it</a>.

<a href='https://github.com/freecodecamp/guides/blob/master/README.md' target='_blank' rel='nofollow'>This quick style guide will help ensure your pull request gets accepted</a>.

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
