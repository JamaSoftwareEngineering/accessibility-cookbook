# Custom Checkbox

**If possible, use a native checkbox with custom CSS. If not possible, try to argue for using it. If you 
just can't because of a particular use case or other reason, then keep reading.**

1. Add `role="checkbox"` to the element simulating the checkbox (receives click events). 
2. Add `aria-checked="true|false|mixed"` to the same element, matching current checked state.
3. Add `tabindex="0"` to allow this element to get focus.
4. Add `cursor:pointer` to the element's styles.
4. If your checkbox is disabled, 
   - Add `aria-disabled` 
   - Provide styling to visually indicate the disabled state (e.g., grayed out)
   - Set `tabindex="-1"` to prevent focus
3. Listen for these events on the element:
   - `click` and keep track of the value in your internal store
   - `keypress` and let users toggle the checked state and value when pressing `SPACE`

## Example

```html
<fieldset role="group">
   <div id="fruit" class="custom-checkbox"
      tabindex="0" role="checkbox" aria-checked="mixed"></div>
   <label for="fruit">Fruit</label>

   <div class="checkbox-group">
      <div id="apples" class="custom-checkbox" 
         tabindex="-1" role="checkbox" aria-checked="true"></div>
      <label for="apples">Apples</label>

      <div id="bananas" class="custom-checkbox" 
         tabindex="-1" role="checkbox" 
         aria-disabled="true" aria-checked="false"></div>
      <label for="bananas">Bananas</label>
   </div>
</fieldset>
```

```css
.custom-checkbox {
   cursor: pointer;
}

.custom-checkbox[aria-disabled] {
   opacity: .5;
   pointer-events: none;
}
```

## References

* https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_checkbox_role 


