# Landmarking

To help AT users get around a page, it's essential to "landmark" a page, adding tags, `roles`, 
and/or other attributes to properly label parts of the page so they are announced properly in 
any AT.

## The Basics

Adding `role` to tags helps AT such as screenreaders understand some of the meaning of that part
of the page. For example, that a list of links is navigation for the page or site. Certain HTML5 
tags, such as ARTICLE, MAIN, NAV, or SECTION have implicit roles.

By using either an HTML5 tag, such as SECTION, NAV, or FORM, or by using a `role` attribute with
a specific, pre-defined value (such as "navigation" or "region"), you help AT users move around 
the page.

| Role   | Tag? | Notes |
| --     | --   | --    |
| `region` | SECTION | Must have a label (`aria-label` or `aria-labelledby`) |
| `form` | FORM | Should have a label with `aria-label` or `aria-labelledby` |
| `search` | none | Usually applied to FORM elements |
| `main` | MAIN | Can have more than one MAIN, but need unique IDs |
| `navigation` | NAV | Identify groups of links used for navigation |
| `banner` | HEADER  | Only a banner when a descendant of BODY |
| `complementary` | ASIDE | Content is similar to main content, but can stand alone. Should use `region` if content is not related to main content. |
| `contentinfo` | FOOTER | Use for the block container with copyright, privacy, terms of use, etc |

## A Word about Labelling

Take care when giving a label to landmarks. *It's not necessary to include the role in 
the label.* Some AT will announce the label with the type of landmark appended to it. For example, 
the following gets announced as "Main navigation navigation."  

```html
<ul role="navigation" aria-label="Main navigation">
...
</ul>
```

This would be a better label:

```html
<ul role="navigation" aria-label="Main">
...
</ul>
```

## Examples

```html
<form role="search" aria-label="Site">
   <input type="text" name="query" title="Query"  />
   <input type="submit" value="Submit"/>
</form>

```


## References

* https://www.w3.org/TR/wai-aria-practices/examples/landmarks
