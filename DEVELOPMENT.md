# DEVELOPMENT

## About the project

The HTML was generated by using a webserver using mustache templates.
So, if you need to edit something that applies to the whole site
programmer tools will be needed.
See [this](https://github.com/un-modelling/website-development).

_Adding and editing content_ should be able to be done easily via
GitHub's interface.


## Project Decisions

It is written in a very traditional and simple HTML fashion.

Keep Javascript to the minimum. **Preferably none.**

The HTML should be as simple as possible. Any chance to remove classes
or ids should be taken.

Use basic HTML and plenty of CSS. Each `<something>/index.html` has it's
`/stylesheets/<something>.css` counterpart. General styling rules are
applied on `/stylesheets/style.css`.

The project tree is organised to that every page is in and `index.html`
to keep the paths pretty. So they look like this:

    un-modelling.github.io/about

instead of

    un-modelling.github.io/about.html

The `tada/` directory is a whole different bussiness as it depends on
another project. Touch it only if you **really** know what you are doing.


## Coding style

No tabs. Two spaces for indentation.

Inside the `<!-- CONTENT-* -->` tags (see below) indentation is reset to
column 0.

`<p>`s in a single line and NO `<br>`s

```html
<div>
  <p>No blank line **before** this.</p>

  <p>Blank lines around this.</p>

  <p>No blank line **after** this.</p>
</div>
                <== blank line here too
<div>
...
</div>
```

## Adding or editing _content_

**Do not** edit anything above `<!-- CONTENT-STARTS -->` or below `<!-- CONTENT-ENDS -->`

**Do not** remove those lines as they are useful for the site's non-content development.

This is a

```html
<!doctype html>

<html>
  <head>...</head>

  <body>
    <nav>...</nav>

    <main>
<!-- CONTENT-STARTS -->

<!-- THIS IS THE TEMPLATE FOR THE RELEVANT ELEMENTS OF THE PAGE.
<section>
  <p>I am a template.</p>
-->

<section>
  <p>All content is contained between CONTENT-STARTS and CONTENT-ENDS.</p>
</section>

<!-- CONTENT-ENDS -->
    </main>

    <footer>...</footer>
  </body>
</html>
```
