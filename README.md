# YSS: CSS for JS fetishistas
YSS aims to be a reference on how to write CSS comments, similar in spirit to 
[KSS](https://github.com/kneath/kss) but more in line with 
[jsDoc](http://usejsdoc.org/). This offers a way to write maintainable styles 
with multiple people working on the same codebase.

## Syntax
````css
@class           - define which css classes are used
@selector        - define which selector this component affects
@state {state}   - define alternate states that are accounted for, e.g. :hover, :selected
@param {param}   - define the variables the class uses, e.g. Number, Color, Mixed
````

## Examples

### File headers
````css
/**
 * Form submit button
 *
 * @class .button-submit
 * @class .button-submit__error
 * @class .button-submit__success
 * @class .button-submit__disabled
 */
````

### Class headers
````js
/**
 * Form submit button text
 *
 * @selector a p > href
 * @state {:hover}
 * @state {:selected}
 * @param {Color} --color-white
 */
````

## License
[MIT](https://tldrlegal.com/license/mit-license) © [Yoshua Wuyts](yoshuawuyts.com)