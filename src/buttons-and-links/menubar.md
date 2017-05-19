# Menubar

## For the menu
0. Use UL and LI 
1. Assign `id` to the LIs. 
1. Add `role="navigation"` to UL 
2. Add `aria-activedescendant` to UL and set to the `id` of the active LI. 

### If you have valid resource or route for the menuitem links
0. Use A. No `title` necessary if the link is text. 

### If the menuitems have scripted click handling
0. Use BUTTON. No `title` necessary if the button contains text. 

## Example 1: Menu with standard text links

```html
<ul role="navigation" aria-activedescendant="my-menu-foo">
  <li id="my-menu-foo">
    <a href="/foo">Foo</a>
  </li>
  <li id="my-menu-bar">
    <a href="/bar">Bar</a>
  </li>
  <li id="my-menu-baz">
    <a href="/baz">Baz</a>
  </li>
</ul>

```

## Example 2: Menu with text links that trigger scripted actions
```html
<ul role="navigation" aria-activedescendant="my-menu-foo">
  <li id="my-menu-foo">
    <button>Foo</button>
  </li>
  <li id="my-menu-bar">
    <button>Bar</button>
  </li>
  <li id="my-menu-baz">
    <button>Baz</button>
  </li>
</ul>

```
