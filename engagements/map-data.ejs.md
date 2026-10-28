```{=html}
<div class="engagement-map-records">
<% for (const item of items) { %>
  <% if (item.location) { %>
  <div class="engagement-map-record"
       data-location="<%= item.location %>"
       data-country="<%= item.country || '' %>"
       data-title="<%= item.title %>"
       data-date="<%= item.date || '' %>"
       data-url="<%= item.path %>"></div>
  <% } %>
<% } %>
</div>
```
