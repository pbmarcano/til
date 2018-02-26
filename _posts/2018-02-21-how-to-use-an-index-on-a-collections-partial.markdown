---
layout: post
title: "How to use an index on a Collection's Partial"
date: "2018-02-21 14:20:14 -0500"
categories: rails
---

When iterating through a collection in a rails view, typically use a block to do so right in my view. 

If I need different id's in the DOM for each element, it's quickly achievable with the `with_index` method which provides the index of each item as it iterates.

```erb
<!-- index.html.erb -->
<ul>
  <% @products.each.with_index do |product, index| %>
    <li id="product<%= index %>"><%= product.name %></li>
  <% end %>
</ul>
```

While `with_index` works when you're iterating through a collection within your view, you but how would you create different id's in the DOM if you're rendering your collection within a partial?

According to [Local variables in Rails documentation](http://guides.rubyonrails.org/layouts_and_rendering.html#local-variables), when you're rendering a collection with a Rails partial, you can use a `counter` as you iterate over that collection.

That same example rendering the collection with a rails partial would look like.

```erb
<!-- index.html.erb -->
<ul>
  <% render partial: "product", collection: @products %>
</ul>

<!-- _product.html.erb -->
<li id="product<%= product_counter %>"><%= product.name %></li>
```
