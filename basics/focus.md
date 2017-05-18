# Focus

* Keep your elements ordered logically in the DOM. Use CSS to adjust 
  visual presentation of their location. A logical order keeps your
  tab focus order logical, too.
* `tabindex="0"` on an element makes in focusable in the natural order of the 
  markup of its page. By following the natural order, tabbing in a page will feel
  _right_.
* `tabindex="-1"` takes the element out of the focus tree for the page.
* **Don't set `tabindex` to anything greater than 0.** This blows up the natural tabbing 
  order. Make your life easy by sticking to the order. If you do need to set
  a custom `tabindex`, then handle the TAB and SHIFT-TAB events properly to set
  focus.

## Dealing with the Outline, aka the Blue Ring

It's not unusual for an app's or site's design to change or disable the default 
focus ring style (setting `outline: none`) because the ring appears during mouse 
interactions, too. Doing so makes the UI harder to use with a keyboard, though. 

You have a few options:

* Leave the default styles and live with the ring. 
* Style the ring to something acceptable for your project.
* Add a `:focus` style that matches your `:hover` style 
* Wait for the proposed `:focus-ring` selector to become widely adopted and 
  use it.
* Use the polyfill for `:focus-ring`. https://github.com/WICG/focus-ring

## References

* http://a11yproject.com/posts/never-remove-css-outlines/
* https://developers.google.com/web/fundamentals/accessibility/focus/
* https://developers.google.com/web/fundamentals/accessibility/accessible-styles
* https://github.com/WICG/focus-ring




