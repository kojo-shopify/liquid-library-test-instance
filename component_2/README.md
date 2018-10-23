# Component 2
Phasellus non consequat velit. Nulla finibus enim a lacus ultricies lacinia. Integer posuere quis elit at dignissim. Nunc pellentesque ex vitae tortor ultrices efficitur. Phasellus euismod erat vitae porta malesuada. Vivamus rhoncus pulvinar maximus. Sed augue sapien, maximus et odio in, vehicula ultrices ligula. 

 ## Table of contents
1. [Breadcrumb Navigation](#breadcrumb-navigation) 
 
 
------
### <a name="breadcrumb-navigation">Breadcrumb Navigation</a>
A Breadcrumb navigation or breadcrumbs, can reduce the number of actions a visitor needs to take in order to navigate to a higher-level page, and improve the discoverability of a website’s sections and pages. Like all navigations, this uses the [linklist] (https://help.shopify.com/en/themes/liquid/objects/linklist) object.

1.  Place the following code in the `theme.liquid` file, just inside the main content wrapper, or wherever you wish the breadcrumb to appear.
2.  Another step that *uses* markdown.

```liquid
{% unless template == 'index' or template == 'cart' or template == 'list-collections' or template == '404' %}
{% assign t = template | split: '.' | first %}
<nav class="breadcrumbs" role="navigation" aria-label="breadcrumbs">
  <ol>
    <li><a href="/" title="Home">Home</a></li>
  {% case t %}
  {% when 'page' %}
    <li><a href="{{ page.url }}" aria-current="page">{{ page.title }}</a></li>
  {% when 'product' %}
    {% if collection.url %}
      <li> {{ collection.title | link_to: collection.url }}</li>
```
`#navigation` `#linklist` 
