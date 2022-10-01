# Bootstrap

## Grid & Responsiveness

Content should adjust to the screen size. You should have one website that can use whatever space is available.

Bootstrap uses the grid (rows and columns) to achieve this (see what happens when you inspect and choose a different device).

Start with a `<div class="container"`.

* Will start with some margin
* Use `class="container-fluid` to take up the full width

### Rows & Columns

Rows have 12 units of width the play with. Columns can be sized specifically by unit or will autofill the row with whatever space is available.

```html
<div class="row">
    <div class="col-4">Col 1</div>
    <div class="col-5">Col 2</div>
    <div class="col">Col 3</div>
</div>
```

> In this example, Col 3 will autofill the remaining space (3 units)

If we overflow the units, a column will be bumped below into the next row, pushing down any rows that follow.

```html
<div class="row">
    <div class="col-8">Col 1</div>
    <div class="col-8">Col 2</div>
</div>
<div class="row">
    <div class="col-8">Col 3</div>
    <div class="col-8">Col 4</div>
</div>
```
> In this example, each column will be presented on its own line (4 rows)

We can also specify the width given variable screensizes using breakpoints

```html
<div class='row'>
    <div class='col-lg-8 col-md-6'>col-lg-8 col-md-6</div>
    <div class='col-lg-4 col-md-6'>col-lg-4 col-md-6</div>
</div>
```
> In this example, when the screen size is large, the columns will be 8 and 4 units wide. When the screen size is medium, the columns will each be 6 units wide. For smaller screen sizes, they will each autofill the entire row.

### Breakpoints
* `-x-small`   | <576 px
* `-small`     | >=576 px
* `-medium`    | >=768 px
* `-large`     | >=992 px
* `-x-large`   | >=1200 px
* `-xx-large`  | >=1400 px

## Colors

The following color suffixes can be used for `text-`, `bg-`, `btn-` and more!

`-primary`
`-secondary`
`-info`
`-success`
`-danger`
`-dark`
`-light`
`-warning`
`-muted`

## Navigation

Start with a `<nav>` component with the following classes
* `navbar` - required
* `.navbar-expand{-sm|-md|-lg|-xl|-xxl}` - [optional] responsive collapsing
* `bg-light` - [optional] light background color for the navbar
* `justify-content-center` - [optional] centers the content

```html
<nav class='navbar navbar-expand-sm bg-light justify-content-center'>
    <ul class='navbar-nav'>
        <li class='nav-item'>
            <a class='nav-link' href='#'>Home</a>
        </li>
        <li class='nav-item'>
            <a class='nav-link' href='#'>Projects</a>
        </li>
        <li class='nav-item'>
            <a class='nav-link' href='#'>Contact</a>
        </li>
    </ul>
</nav>
```

Use a `<ul>` to contain the list of navigation links
* `navbar-nav` - a full-height and lightweight navigation (including support for dropdowns).

Each navigation link is an `<a>` tag nested inside an `<li>`
* `nav-item` used for the `<li>` - required
* `nav-link` used for the `<a>` - required



