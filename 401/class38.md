# More React
## Conditional Rendering

1. Using an if…else Statement
An if…else statement will execute the actions contained in the if block when the condition is satisfied. Otherwise, it will execute the actions contained in the else block.

In JSX, you are able to use JavaScript code with markup to render dynamic values within your application. JSX uses curly braces ({ and }) to signify expressions that need to be interpreted prior to rendering. The caveat, however, is that there is a limit to what can be done within such braces.

Let’s consider if you were to attempt to use an if…else statement in the render() method:

Warning: This is an example of code that will not work properly. It is presented as an example of the limitations of interpretation in the render() method.

// ...

```
class App extends Component {
  // ...

  render() {
    let {isLoggedIn} = this.state;

    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        {
          if(isLoggedIn){
            return <button>Logout</button>
          } else{
            return <button>Login</button>
          }
        }
      </div>
    );
  }
}

// ...
 ```
This code would produce an Unexpected token error. The logic will need to be moved outside of the render() method.

Open the App.js file in your code editor, scroll down to the render() method and make the following highlighted code changes:

src/App.js
// ...
```
class App extends Component {
  // ...

  render() {
    let {isLoggedIn} = this.state;

    const renderAuthButton = () => {
      if (isLoggedIn) {
        return <button>Logout</button>;
      } else {
        return <button>Login</button>;
      }
    }

    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        {renderAuthButton()}
      </div>
    );
  }
}
```
// ...
 
This is the process of creating an extracted function. This code extracts the logic from JSX into a function renderAuthButton. And the function is executed within the JSX curly braces.

Open your application in your web browser. Previously, the Login and Logout buttons were displayed. Now, the isLoggedIn state is true and the conditional logic results in only the Logout button displayed.

Now, let’s consider if you were to attempt to use multiple returns in the render() method instead:

Warning: This is an example of poorly performant code that should be avoided.

// ...
```
class App extends Component {
  // ...

  render() {
    let {isLoggedIn} = this.state;

    if (isLoggedIn) {
      return (
        <div className="App">
          <h1>
            This is a Demo showing several ways to implement Conditional Rendering in React.
          </h1>
          <button>Logout</button>
        </div>
      );
    } else {
      return (
        <div className="App">
          <h1>
            This is a Demo showing several ways to implement Conditional Rendering in React.
          </h1>
          <button>Login</button>
        </div>
      );
    }
  }
}

// ...
 ```
The snippet above would achieve the same result but bloat the component unnecessarily while introducing performance issues as a result of constantly re-rendering an unchanging component.

The best practice is to keep components as simple as possible to avoid a wasted re-render of sibling or parent components.

In your code editor, create a new AuthButton.js file:
```
src/AuthButton.js
import React from "react";

const AuthButton = props => {
  let { isLoggedIn } = props;

  if (isLoggedIn) {
    return <button>Logout</button>;
  } else {
    return <button>Login</button>;
  }
};

export default AuthButton;
``` 
AuthButton returns various elements or components depending on the value of state that is passed down via the isLoggedIn props.

Next, revisit App.js and modify it to use the new component:
```
src/App.js
import React, { Component } from "react";
import './App.css';
import AuthButton from "./AuthButton";

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      isLoggedIn: true
    };
  }

  render() {
    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        <AuthButton isLoggedIn={isLoggedIn} />
      </div>
    );
  }
}

export default App;
 ```
This is the process of creating an extracted functional component. This code produces the same result as the renderAuthButton() approach. but has the advantage of moving the changes to a separate component.

2. Using a switch Statement
As shown previously, you can conditionally return different markup from a component based on set conditions using an if…else statement. The same could be achieved with a switch statement where you can specify the markup for various conditions.

Revisi the AuthButton component and replace the if…else statement with a switch statement:
```
src/AuthButton.js
import React from "react";

const AuthButton = props => {
  let { isLoggedIn } = props;

  switch (isLoggedIn) {
    case true:
      return <button>Logout</button>;
      break;
    case false:
      return <button>Login</button>;
      break;
    default:
      return null;
  }
};

export default AuthButton;
 ```
Notice how this code returns various buttons based on the value of isLoggedIn.

Note: It would be more practical to apply the switch statement method when there are more than two possible values or outcomes.

Furthermore, returning null from a component will cause it to hide itself (display nothing). This a good way to toggle the visibility of components.

3. Using Element Variables
Element variables are similar to the approach to extract the conditional rendering into a function. Element variables are variables that hold JSX elements. You can conditionally assign elements or components to these variables outside the JSX and only render the variable within JSX.

The application could be rewritten like this:
```
src/App.js
import React, { Component } from "react";
import './App.css';

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      isLoggedIn: true
    };
  }

  render() {
    let { isLoggedIn } = this.state;
    let AuthButton;

    if (isLoggedIn) {
      AuthButton = <button>Logout</button>;
    } else {
      AuthButton = <button>Login</button>;
    }

    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        {AuthButton}
      </div>
    );
  }
}

export default App;
 ```
Notice how this code conditionally assigns values - components - to AuthButton and then it can be referenced later in the JSX.

4. Using Ternary Operators
The conditional (ternary) operator is the only JavaScript operator that takes three operands. This operator is frequently used as a shortcut for the if statement.

The application could be rewritten like this:
```
src/App.js
import React, { Component } from "react";
import './App.css';

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      isLoggedIn: true
    };
  }

  render() {
    let { isLoggedIn } = this.state;

    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        {isLoggedIn ? <button>Logout</button> : <button>Login</button>}
      </div>
    );
  }
}

export default App;
 ```
In cases where, this approach makes the component bloated, bulky, or less readable, you may encapsulate the conditional within a functional component:
```
src/AuthButton.js
import React from "react";

const AuthButton = props => {
  let { isLoggedIn } = props;

  return isLoggedIn ? <button>Logout</button> : <button>Login</button>;
};

export default AuthButton;
 ```
The ternary approach is useful for uncomplicated if…else evaluations. For complicated comparisons and components, it may impact readability as a project grows.

5. Using Logical && (Short Circuit Evaluation)
Short circuit evaluation is a technique used to ensure that there are no side effects during the evaluation of operands in an expression. The logical && helps you specify that an action should be taken only on one condition, otherwise, it would be ignored entirely.

The application could be rewritten like this:
```
src/App.js
import React, { Component } from "react";
import './App.css';

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      isLoggedIn: true
    };
  }

  render() {
    let { isLoggedIn } = this.state;

    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        {isLoggedIn && <button>Logout</button>}
      </div>
    );
  }
}

export default App;
 ```
This code would display the Logout button if isLoggedIn is true, otherwise it would display nothing.

Now, let’s consider using a second short circuit evaluation for the Login button:

Warning: This is an example of poorly performant code that should be avoided.

{isLoggedIn && <button>Logout</button>}
{!isLoggedIn && <button>Login</button>}
 
This code would render the right button based on the value of isLoggedIn. However, this is not recommended because there are better, cleaner ways to achieve the same effect. As your application grows, this overuse of short circuit evaluation may become cumbersome and unintuitive.

6. Using Immediately Invoked Function Expressions (IIFEs)
Earlier sections mentioned that JSX limitations make it unable to execute every type of JavaScript code. It is possible to bypass these limitations with Immediately Invoked Function Expressions (IFFEs). IFFEs is a JavaScript function that runs as soon as it is defined:
```
(function () {
  // statements
})();
 
With this technique, you are able to write conditional logic directly within JSX but wrapped within an anonymous function that is immediately invoked on the evaluation of that code.

The application could be rewritten like this:

src/App.js
import React, { Component } from "react";
import './App.css';

class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      isLoggedIn: true
    };
  }

  render() {
    let { isLoggedIn } = this.state;

    return (
      <div className="App">
        <h1>
          This is a Demo showing several ways to implement Conditional Rendering in React.
        </h1>
        {(function() {
          if (isLoggedIn) {
            return <button>Logout</button>;
          } else {
            return <button>Login</button>;
          }
        })()}
      </div>
    );
  }
}

export default App;
 ```
This can also be written in a slightly more concise manner using an arrow function:
```
{(() => {
  if (isLoggedIn) {
    return <button>Logout</button>;
  } else {
    return <button>Login</button>;
  }
})()}
```
