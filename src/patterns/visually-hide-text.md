# Visually Hide Text

Sometimes, you want an element to be available to AT, but to be visually
hidden on screen. For that, you can apply a `.visually-hidden` CSS class
with the following styles.

```css
.visually-hidden {
  position: absolute !important;
  clip: rect(1px 1px 1px 1px); /* IE6, IE7 */
  clip: rect(1px, 1px, 1px, 1px);
  padding:0 !important;
  border:0 !important;
  height: 1px !important;
  width: 1px !important;
  overflow: hidden;
}
```


## Example

```html
<div aria-live="polite" class="visually-hidden">
  File saved successfully.
</div>
```

## References

* https://developer.yahoo.com/blogs/ydn/clip-hidden-content-better-accessibility-53456.html
