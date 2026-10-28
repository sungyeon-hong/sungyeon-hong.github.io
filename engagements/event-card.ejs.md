```{=html}
<div class="event-listing-grid list">
<% for (const item of items) { %>
  <article class="event-listing-card" <%= metadataAttrs(item) %>>
    <% if (item.image) { %>
    <a class="event-listing-image-link" href="<%- item.path %>" aria-label="Open <%- item.title %>">
      <img class="event-listing-image" src="<%- item.image %>" alt="">
    </a>
    <% } %>

    <div class="event-listing-body">
      <h3 class="event-listing-title listing-title">
        <a href="<%- item.path %>"><%= item.title %> <span class="external-arrow" aria-hidden="true">↗</span></a>
      </h3>

      <div class="event-listing-date-row">
        <span class="event-meta-label">DATE</span>
        <time class="event-listing-date listing-date"><%= item.date %></time>
      </div>
      <% if (item.location) { %>
      <div class="event-listing-location-row">
        <span class="event-meta-label">LOCATION</span>
        <span class="event-listing-location listing-location"><%= item.location %></span>
      </div>
      <% } %>

      <% if (item.description) { %>
      <p class="event-listing-description listing-description"><%= item.description %></p>
      <% } %>

      <% if (item.categories && item.categories.length) { %>
      <div class="event-listing-categories">
        <% for (const category of item.categories) { %>
        <span class="listing-category"><%= category %></span>
        <% } %>
      </div>
      <% } %>
    </div>
  </article>
<% } %>
</div>
```
