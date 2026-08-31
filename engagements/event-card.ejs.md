```{=html}
<div class="event-listing-grid list">
<% for (const item of items) { 
     const organisers = Array.isArray(item.organisers)
       ? item.organisers.join(" · ")
       : item.organisers;
%>

<article <%- metadataAttrs(item) %> class="event-listing-card">

  <h3 class="event-listing-title">
    <a href="<%= item.path %>"><%= item.title %></a>
  </h3>

  <% if (item.date) { %>
  <div class="event-listing-date-row">
    <span class="event-listing-label">DATE</span>
    <span class="event-listing-date"><%= item.date %></span>
  </div>
  <% } %>

  <% if (item.description) { %>
  <p class="event-listing-description"><%= item.description %></p>
  <% } %>

  <% if (item.categories && item.categories.length) { %>
  <div class="event-listing-tags">
    <% item.categories.slice(0, 2).forEach(function(category) { %>
      <span><%= category %></span>
    <% }) %>
  </div>
  <% } %>

</article>
<% } %>
</div>
```
