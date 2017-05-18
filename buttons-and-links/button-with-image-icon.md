# Button with Image or Icon

1. Add `title` to the BUTTON with a value of text that describes the purpose of the button.
2. Add `aria-hidden="true"` on the I or IMG element. 

If the button contains text in addition to the icon or image, you do not need to add the `title`
to BUTTON, but you do need to keep the `aria-hidden` on the icon or image.

## Example 1: Button with icon as content
```html
<button title="Edit document">
   <i class="fa-edit" aria-hidden="true" />
</button>
```

## Example 2: Button with icon + text as content
```html
<button>
   <i class="fa-edit" aria-hidden="true" />
   Edit Document
</button>
```
