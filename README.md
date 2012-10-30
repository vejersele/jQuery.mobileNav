jQuery.mobileNav
================

###jQuery.mobileNav?###
You can use this plugin to create an easy to use mobile navigation for your responsive website. 

###html###

```html
<nav id="primaryNav">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Work</a></li>
    <li class="active"><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
````
###javascript###

```javascript
$(function () {
  $('#primaryNav').mobileNav();  
});
```

###options###

```javascript
{
  // css classes
  css: {
    triggerClass: "mobileNavTrigger",
    pluginActiveClass: "mobileNavActive",
    isOpenClass: "mobileNavOpen",
    labelClass: "mobileNavLabel",
  },

  // text settings
  text: {
    openText: "Open menu",
    closeText: "Close menu",
    noActiveItemText: "Menu"
  },

  // available callbacks
  callbacks: {
    afterOpen: undefined, 
    afterClose: undefined,
    afterConstruct: undefined,
    afterDestruct: undefined,
  },

  breakpoint: 500, // $(window).width() value
  showLabel: false, // show a label with the active menu item
  activeItemSelector: "ul > li.active > a" // selector to get the active menu item
}
```

###methods###
```javascript
$('#primaryNav').mobileNav('updateLabel'); // updates the label. Can be useful when using ajax ...
```