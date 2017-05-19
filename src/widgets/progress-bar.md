# Loading Progress Bar

1. Create a PROGRESS element.
2. Set the progress bar's values:
   - If determinate, add `max`, and `value` attributes.
   - If indeterminate, omit the `value` attribute.
3. Create a DIV with `aria-live="polite"`. This is a live region to announce updates.
4. As your progress updates, update the `value` on the PROGRESS and the text content 
   of the DIV live region.

> Use the `:indeterminate` CSS pseudo-class to style the PROGRESS element

## Example 1: Determinate progress bar

```html
<progress max="100" value="35">35%</progress>
<div aria-live="polite">Loading progress: 35%</div>
```
## Example 2: Indeterminate progress bar

```html
<progress max="100"></progress>
<div aria-live="polite">Downloading assets</div>
```

## Example 3: Non-HTML5 progress bar

```html
<div role="progressbar" 
   aria-minvalue="0" 
   aria-maxvalue="100" 
   aria-value="35">35%</div>
<div aria-live="polite">Downloading assets</div>
```


## References

* https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress
* https://labs.ssbbartgroup.com/index.php/Progress_Bar_with_ARIA_Live_Regions
* http://caniuse.com/#feat=css-indeterminate-pseudo
