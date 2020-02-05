<template>
  <div>
    <!-- Navigation -->
    <div class="header-wrapper">
      <header class="header layout">
        <strong>
          <g-link to="/">{{ $static.metadata.siteName }}</g-link>
        </strong>
        <nav class="nav">
          <g-link class="nav__link" to="/">Home</g-link>
          <g-link class="nav__link" to="/blog/">Blog</g-link>
        </nav>
      </header>
    </div>

    <!-- Inserted content -->
    <div class="content layout">
      <slot />
    </div>

    <!-- Footer -->
    <div class="footer-wrapper">
      <footer class="footer layout">
        <strong>
          <p>{{$static.metadata.siteName }} &copy; {{ new Date().getFullYear()}}</p>
        </strong>
      </footer>
    </div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
:root {
  --accent-color: #a731eb;
  --border-color: #b1b1b1;
}
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
  background: #ffffff;
  border: 4px solid var(--accent-color);
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.content {
  /* to make the everything on some pages  visiblbe without scrolling */
  min-height: calc(100vh - 120px);
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
}
.header-wrapper {
  border-bottom: 2px solid var(--border-color);
  margin-bottom: 20px;
}

.footer {
  text-align: center;
  height: 40px;
}
.footer-wrapper {
  border-top: 2px solid var(--border-color);
}

.nav__link {
  margin-left: 20px;
}
a {
  color: var(--accent-color);
}
img {
  max-width: 100%;
}
</style>
