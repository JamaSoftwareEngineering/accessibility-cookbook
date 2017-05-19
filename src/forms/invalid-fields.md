# Invalid Fields

1. Add `aria-invalid="true"` to the invalid INPUTs.
2. Add `aria-describedby` to the invalid INPUTs. Set the value to the appropriate error message text.

## Example

```html
<form aria-label="Account Sign-Up">
   <label for="username">Username</label>
   <input type="text" id="username" 
      aria-describedby="Username is required."
      aria-invalid="true" />
   ...
</form>
```

## References

* http://webaim.org/techniques/formvalidation/
