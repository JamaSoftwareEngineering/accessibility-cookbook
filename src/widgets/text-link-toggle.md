# Text Link Toggle

Create a text link that show/hides a container when clicked.

1. Create a BUTTON with text for the link. Style it to look like a plain text link.
2. Create a DIV, SECTION, or other tag to hold the content that is shown/hidden.
   - If you didn't use a SECTION tag, add `role="region"` to this element.
4. Add an `id` and `aria-expanded="false"` for this content element.
5. On the BUTTON, add `aria-controls` and set its value to the id of the content element. 
6. Update `aria-expanded` to match the shown/hidden state as it's toggled.
7. When toggling the content visible, set focus on the content element.

## Example

```html
<p>View your 
   <button class="text-link" aria-controls="group-conversations">
      5 group conversations
   </button>.
</p>
<section id="group-conversations" aria-expanded="false" class="hidden">
   ...
</section>
```

```html
<p>View your 
   <button class="text-link" aria-controls="group-conversations">
      5 group conversations
   </button>.
</p>
<section id="group-conversations" aria-expanded="true" class="">
   ...
</section>
```

## References

* http://oaa-accessibility.org/example/20/
