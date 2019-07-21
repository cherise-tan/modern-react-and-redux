# Section 2 - Building Content with JSX

## JSX
* JSX is a special dialect of JavaScript (not HTML)
* JSX code gets converted into a JavaScript function call by Babel
    * Simpler to read/write as JSX than as a JavaScript function, especially as content gets more complex
* When returning a React component, need to show that there is something that follows the 'return' statement, therwise this will return an 'undefined/
    ```
    const App = () => {
        return <div>
        .....
    };
    ```
    OR
    ```
    const App = () => {
        return (
            <div>...</div>
        );
    };
    ```

## JSX Conventions
    * Use "" whenever we want to indicate a STRING / for JSX properties
    * Use '' for any non-JSX property

## Converting HTML to JSX
* JSX is very similar in form and function to HTML, with a couple of differences:
    * Adding custom styling to an element uses different syntax
        * HTML: ```<div style="background-color: red;">```
        * JSX: ```<div style={{backgroundColor: 'red'}>```
            * The outer '{}' indicates we want to reference a JavaScript variable inside of our JSX
            * The inner '{}' indicates a JavaScript object - where all the KEYS of the object reference a different property to by styles, and the VALUES indicate the value for that particular styling
            * Remove the '-' and camelCase the property name instead
    * Adding a class to an element uses different syntax 
        * HTML: ```class="..."```
        * JSX: ```className="..."```
        * This is on order to prevent conflicts with the keyword 'class' that is used in JSX to define a JavaScript Class
    * JSX can reference JS variables
        * Can easily take a JS variable and display it within our JSX block within a set of curly braces '{}'
        ```
        // Referencing a variable
        const App = () => {
            const buttonText = 'Click Me';
            return <button>{buttonText}</button>
        }
        ```
        OR
        ```
        // Referencing a function
        function getButtonText(){
            return 'Click on me!';
        }
        const App = () => {
            return <button>{getButtonText()}</button>
        }
        ```
    * Values JSX can show:
        * Strings, Numbers, Arrays
    * Values JSX can't show:
        * JavaScript Objects: ```const buttonText = { text: 'Click Me'};```
            * JS Objects are not valid as a React child -> cannot reference it within JSX, specifically where we display text
            * Can reference a property of an object however: ```{buttonText.text}```
        * JS Objects can be used as long as we aren't trying to display them as text

### Finding Forbidden Property Names
* Reference the Console (within Dev Tools) to intermittently check whether you are using any forbidden names -> these may not crash your program, but may cause other issues
    * Good to just keep the Console open when you are developing