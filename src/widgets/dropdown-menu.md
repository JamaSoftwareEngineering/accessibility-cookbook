# Dropdown Menu

Create a button that when clicked reveals a menu with several options.

## Keyboard and Focus

0. SPACE and ENTER on the menu activator to toggle it. BUTTON gives you
   this behavior natively.
1. TAB/SHIFT-TAB between menu items. SPACE and ENTER to select it.
2. When the menu is open, you shouldn't be able to TAB away from it. TAB from
   the last menu item sets focus on the first menu item, and vice versa.
2. ESC closes the menu.
3. On closing, return focus to the menu activator.

## Styling

Take advantage of the aria attributes in your CSS to set styling. Often the attribute 
indicates something you might have written a class for, such as `aria-expanded` 
instead of `.expanded`.

## Example

```html
<div id="fruit-menu" class="dropdown-menu" aria-haspopup="true">

  <button id="fruit-menu-activator" 
      class="dropdown-menu-activator"
      aria-controls="fruit-menu-options">
      Fruit
    <i class="fa fa-toggle-down" aria-hidden="true"></i>   
  </button> 
  
  <ul id="fruit-menu-options" role="menu" aria-expanded="false">
      <li role="menuitem">
         <button>Apples</button>
      </li>
      <li role="menuitem">
         <button>Banana</button>
      </li>
      <li role="menuitem">
         <button>Kiwi</button>
      </li>
   </ul>
</div>
```

```js
// This is not a complete menu implementation, but a simple example of how 
// you might use aria-attribute toggling to show or hide the menu.

const $menu = document.querySelector('[role=menu]');

document.querySelector('.dropdown-menu-activator')
   .addEventListener('click', () => {
     const expanded = $menu.getAttribute('aria-expanded') === 'true';
     $menu.setAttribute('aria-expanded', !expanded);
   });
```


```scss
// dropdown-menu.scss

.dropdown-menu {
  width: 200px;
  font-size: 1rem;
  
  .dropdown-menu-activator {
    padding: 1em;
    font-size: inherit;
    font-weight: bold;    
  }
    
  [role=menu] {
    list-style: none;
    padding: 0;
    margin: 0;
    display: none;

    &[aria-expanded=true] {
      display: block;
    }
  }
  
  [role=menuitem]  {
    border: 1px solid #ddd;
    border-bottom: none;
    
    &:last-child {
      border-bottom: 1px solid #ddd;
    }   
    
    button {
      background: none;
      border: none;
      padding: 1em;
      display: block;
      width: 100%;
      text-align: left;
      font-size: inherit;
      
      &:hover, &:focus {
        background: skyblue;
      }
    }
  }
}

```

## References

* https://www.w3.org/WAI/tutorials/menus/flyout/
