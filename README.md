# YSS: maintainable CSS annotation
YSS aims to be a reference on how to write CSS comments, similar in spirit to 
[KSS](https://github.com/kneath/kss) using [jsDoc](http://usejsdoc.org/)-esque notation. 
YSS offers a way to write maintainable styles with multiple people working on the same codebase.

If you're looking for a guide on how to structure your css check out [bevacqua/css](https://github.com/bevacqua/css).

## Syntax
````
@class           - define which css classes are used
@selector        - define which selector this component affects
@state {state}   - define alternate states that are accounted for
@param {param}   - define the variables the class uses
````

## Examples

An example YSS block for BEM-style modifiers.
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

An example YSS block for a link with multiple states.
````css
/**
 * Form submit button text
 *
 * @selector a p > href
 * @state {:hover}
 * @state {:selected}
 * @param {Color} --color-submit
 */

a p > href {
  text-decoration: none;
  color: hsla(0, 100, 60%, 1);
}

a p > href:hover,
a p > href:selected {
  color: hsla(0, 100, 80%, 1);
  background-color: var(--color-submit);
}
````

## License
[MIT](https://tldrlegal.com/license/mit-license) © [Yoshua Wuyts](yoshuawuyts.com)