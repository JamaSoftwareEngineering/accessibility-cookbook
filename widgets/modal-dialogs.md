# Modal Dialogs

Modal dialogs (sometimes called *popups*) need special consideration for keyboardability and element focus.

1. Add `role=dialog` to the container element.
1. Add `aria-label` or `aria-labelledby` to the container element, with appropriate value.
2. Add `role=document` to the modal content's container. 
1. When you open a modal, set focus on the element most likely to benefit a user the most, not just the first focusable element in the markup. 
   For example, a modal containing a form with a close button in the upper-right might have markup that makes the close button the first focusable
   element. Because it has a form, though, a better initial focus point is the first non-hidden INPUT.
2. Set a keyboard trap to ensure that users cannot tab away from the modal. Listen for tab keyboard events and re-route when a user
   tabs away from the last focusable element, or shift-tabs away from the first focusable element.
3. Close the dialog when the user presses the ESC key.
4. After closing, return focus to the element that had focus before the modal was opened. `document.activeElement` is a good way
   to track focused elements.

## Example

```html
<div class="modal" role="dialog" aria-labelledby="confirmation-heading">
   <header>
      <h1 id="confirmation-heading">Confirm item deletion</h1>
   </header>
   <div class="modal-body" role="document">
      <p>Your item will be deleted immediately.</p>
   </div>
   <footer>
      <button>Cancel</button>   
      <button class="primary">Delete</button>   
   </footer>
</div>
```


## References

* https://www.w3.org/TR/wai-aria-practices-1.1/#dialog_modal
* https://www.marcozehe.de/2015/02/05/advanced-aria-tip-2-accessible-modal-dialogs/
* https://developer.mozilla.org/en-US/docs/Web/API/Document/activeElement
* https://github.com/ianmcburnie/jquery-keyboard-trap
* https://github.com/gdkraus/accessible-modal-dialog
