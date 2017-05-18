# Link with no HREF

In modern web development, it's common to use A tags with `href="#"` to create text links
that trigger javascripted actions. Unfortunately, this markup gets read by most screenreaders
with the word "link" preprended ("link Home" or "link login").

**If you don't have a true resource to put in the `href`, use a BUTTON styled to look like a 
text link instead.**

By using BUTTON, you preserve keyboardability in your page and AT can handle the element
properly.

## Example

```html
<button class="text-link">
   Open help
</button>
```
