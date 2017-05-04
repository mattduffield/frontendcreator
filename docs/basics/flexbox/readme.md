# Flexbox

Layout has always been a challenge when dealing with CSS and HTML. Flexbox has been out for some time now and is support both across desktop and mobile. Flexbox was used extensively making FrontEnd Creator. There are both container level and child level CSS properties that you can set to achieve the results you are looking for. Flexbox can provide an excellent responsive solution for layout and most modern CSS libraries are embracing it or have it on their roadmap. It is also possible to build complex fixed layout solutions as well using the Flexbox paradigm making it an excellent choice for most of your layout needs.

Let's take a look at the container level CSS classes:

```css
.flex { display: flex; }

.flex-direction-column { flex-direction: column; }
.flex-direction-column-reverse { flex-direction: column-reverse; }
.flex-direction-row { flex-direction: row; }
.flex-direction-row-reverse { flex-direction: row-reverse; }

.flex-wrap-wrap { flex-wrap: wrap; }
.flex-wrap-nowrap { flex-wrap: nowrap; }
.flex-wrap-wrap-reverse { flex-wrap: wrap-reverse; }

.justify-content-center { justify-content: center; }
.justify-content-end { justify-content: flex-end; }
.justify-content-start { justify-content: flex-start; }
.justify-content-space-around { justify-content: space-around; }
.justify-content-space-between { justify-content: space-between; }

.align-items-start { align-items: flex-start; }
.align-items-end { align-items: flex-end; }
.align-items-center { align-items: center; }
.align-items-baseline { align-items: baseline; }

.align-content-start { align-content: flex-start; }
.align-content-end { align-content: flex-end; }
.align-content-center { align-content: center; }
.align-content-space-between { align-content: space-between; }
.align-content-space-around { align-content: space-around; }
.align-content-stretch { align-content: stretch; }
```

As you can see, the CSS classes are simply a means of applying Flexbox properties by adding or removing the classes.

The following is a listing of the child level CSS classes:

```css
.flex-0-0 { flex: 0 0 auto; }
.flex-1-1 { flex: 1 1 auto; }
.flex-1-0 { flex: 1 0 auto; }
.flex-0-1 { flex: 0 1 auto; }
.flex-2-2 { flex: 2 2 auto; }
.flex-2-0 { flex: 2 0 auto; }
.flex-0-2 { flex: 0 2 auto; }
.flex-3-3 { flex: 3 3 auto; }
.flex-3-0 { flex: 3 0 auto; }
.flex-0-3 { flex: 0 3 auto; }
.flex-4-4 { flex: 4 4 auto; }
.flex-4-0 { flex: 4 0 auto; }
.flex-0-4 { flex: 0 4 auto; }
.flex-5-5 { flex: 5 5 auto; }
.flex-5-0 { flex: 5 0 auto; }
.flex-0-5 { flex: 0 5 auto; }

.align-self-auto { align-self: auto; }
.align-self-start { align-self: flex-start; }
.align-self-end { align-self: flex-end; }
.align-self-center { align-self: center; }
.align-self-baseline { align-self: baseline; }
.align-self-stretch { align-self: stretch; }
```

The `.flex-?-?` classes are simply a shorthand for specifying the grow, shrink, and size capabilities of the child.

It is possible to achieve grid layouts like Twitter Bootstrap or Foundation Zurb by simply applying the right set of classes. It is even easier to use Flexbox for layout that are more complex then a simple grid formation.

Consider the following layout. It is possible to create this and with very little amount of HTML and CSS.

![Tutorial Flexbox Preview](../../assets/images/tutorials/tutorial-flexbox.png)

If you are interested in building the previous layout using Flexbox, you can go to the tutorial [ Flexbox Tutorial ](../../tutorials/flexbox-screen.md).

For a list of Flexbox classes provided see [ Flexbox Classes ](../../reference/flexbox-classes.md)

> #### primary::
> Please refer to Flexbox documentation online for further understanding and usage of all the settings.
