# Link with SVG Content

If you need to create a link that has a SVG content, not text or image, as its content, 
you need to do more than add `title` or `aria-label` to allow it to be read by assistive 
technology properly.

1. Add `role=img` and  `aria-label` to the SVG tag. 
2. Set `aria-label` to text that describes the SVG (such as 'Home' for a home icon).
3. Add a TITLE tag with the same text you used for the `aria-label` as its content.
4. The A tag doesn't need a `title` or `aria-label`.

## Example 1: Link with SVG home icon
```html
  <a href="/">
    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
    class="icon-house" viewBox="0 0 388.384 335" xml:space="preserve" role="img" aria-label="Home">
      <title>Home</title>
      <g>
        <polygon points="322.505,101.101 322.505,11.5 268.505,11.5 268.505,47.212 	"/>
        <polygon points="194.193,71.946 65.943,199.931 65.943,335 160.443,335 160.443,227.5 227.943,227.5 227.943,335 322.443,335 322.443,199.931 	"/>
      </g>
      <path d="M22.5,216.338c-5.767,0.001-11.531-2.202-15.926-6.606c-8.778-8.796-8.763-23.042,0.033-31.82L178.299,6.573
      c8.783-8.765,23.004-8.765,31.787,0L381.778,177.91c8.796,8.778,8.811,23.024,0.033,31.82c-8.78,8.795-23.024,8.81-31.82,0.033
      L194.193,54.287L38.394,209.764C34.002,214.146,28.25,216.338,22.5,216.338z"/>' +
    </svg>
  </a>
```
