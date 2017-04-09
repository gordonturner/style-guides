JavaScript-style-guide
======================

- Best practices:
http://learn.jquery.com/style-guide/
http://contribute.jquery.org/style-guide/js/ 
https://github.com/stevekwan/best-practices/blob/master/javascript/gotchas.md
    

Comments
--------

- Inline comments should have a leading space and be complete sentences.
- Example:
```
\\ Bind the click event to the function.
```

- Use JSDoc comments: 
http://usejsdoc.org/
https://github.com/jsdoc3/jsdoc

- Use @name, @constructor, @param, and @returns.
http://usejsdoc.org/tags-name.html
http://usejsdoc.org/tags-constructor.html
http://usejsdoc.org/tags-param.html
http://usejsdoc.org/tags-returns.html

- Include a description of the object, full sentence.
- Example:
```
/*-----------------------------------------------------------------------------*/
 * The ReferencePlugin object.
 * 
 * @constructor
 * @param {string}
 *          id - Id of the div to target for html replacement.
 * @param {int}
 *          interval - How often to run update() to refresh the content.
 * @param {string}
 *          exampleParameter - Parameter that will be printed out later in a method.
 *
 * @return {string}
 *           returnValue - What gets return, null if nothing.
 */
function ReferencePlugin( id, interval, exampleParameter ) {
	
}
```

- Place any hacks or quick work arounds in shame.js

- Always run jslint against code before committing.
http://www.jslint.com/
    
    
