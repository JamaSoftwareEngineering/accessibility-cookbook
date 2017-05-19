# Load More List Items

You have a list of items, with a button labelled, "Load More," following the list. 
When clicked, more items are loaded into the list dynamically.

0. Add a DIV with `aria-live="polite"`. This live region will be used to update AT users of
   dynamic changes in the page. The text in this DIV gets read by AT as it changes.
1. After clicking the Load More BUTTON, fetch the data, and set the content of
   the live region to something meaningful, such as _Retrieving more users_. 
2. When the data returns and your list is updated, set the live region content, too. 
   Make the text meaningful, such as _15 more users loaded_.
3. Set focus on the first new item fetched, if it's something actionable.

```html
<ul>
  <!-- Initial items -->
  <li>Apples</li>
  <li>Bananas</li>
  <li>Kiwi</li>
  <!-- Loaded in -->
  <li>Kumquats</li>
  <li>Raspberries</li>
  <li>Oranges</li>
</ul>

<button>Load More</button>

<div aria-live="polite" class="visually-hidden">
  3 more fruit loaded.
</div>
```
