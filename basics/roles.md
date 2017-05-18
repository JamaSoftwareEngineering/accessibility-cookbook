# Roles

Adding `role` with an appropriate value gives meaning to your markup. With the right role, 
AT understands that your UL with LIs is not just a list but `navigation`, or that a combination
of INPUT and UL make a combobox, for example.

```html
<div role="region" aria-labelledby="heading-preferences">
   <div role="status">Preferences saved.</div>
   <h1 id="heading-preferences">Preferences</h1>
   <fieldset>
      <div id="groups" 
         role="combobox" 
         aria-label="Groups" 
         aria-owns="group-list" 
         aria-expanded="false"
         aria-haspopup="true">
         <input type="text" aria-controls="group-list" aria-activedescendant="group-people">
         <ul id="group-list" role="listbox">
            <li role="option" id="group-people">People</li>
            <li role="option" id="group-support">Support</li>
            <li role="option" id="group-sales">Sales</li>
         </ul>
      </div>
      ...
   </fieldset>
</div>
```

There are 4 types of roles that you need to care about that can be applied to elements: 

| Role | Purpose |
| ---- | ------- |
| Document Roles | Indicate structures that organize a page. Not usually interactive. |
| Landmark Roles | Indicate navigational landmarks |
| Widget Roles | Indicate an interactive UI widget or control |
| Live Region Roles | Widget roles that are also live regions and can accept live region attributes |

See [Definition of Roles](https://www.w3.org/TR/wai-aria-1.1/#role_definitions) for more infomation about 
each of the roles on this page.

## Document Roles

These roles indicate document structure.

* application
* article
* cell
* columnheader
* definition
* directory
* document
* feed
* figure
* group
* heading
* img
* list
* listitem
* math
* none
* note
* presentation
* region
* row
* rowgroup
* rowheader
* separator
* table
* term
* toolbar

## Landmark Roles

* banner
* complementary
* contentinfo
* form
* main
* navigation
* region
* search

See [Landmarking](landmarking.md) for more info.

## Widget Roles

Use these roles to indicate a single, independent UI widget or control:

* alert
* alertdialog
* button
* checkbox
* dialog
* gridcell
* link
* log
* marquee
* menuitem
* menuitemcheckbox
* menuitemradio
* option
* progressbar
* radio
* scrollbar
* searchbox
* slider
* spinbutton
* status
* switch
* tab
* tabpanel
* textbox
* timer
* tooltip
* treeitem

### Composite Widget Roles

Use these roles to build a more advanced widget that contains other widgets:

* combobox
* grid
* listbox
* menu
* menubar
* radiogroup
* tablist
* tree
* treegrid

## Live Region Roles

These widget roles also act as live region roles and can accept live region attributes.

* alert
* log
* marquee
* status
* timer

## References

* https://www.w3.org/TR/wai-aria-1.1/#roles_categorization
