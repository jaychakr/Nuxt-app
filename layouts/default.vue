<script setup></script>
<template>
  <div>
    <header>
      <nav>
        <ul>
          <li>
            <NuxtLink to="/about">About</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/blog">Blog</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <slot />
  </div>
</template>
<style scoped>
nav {
  background-color: #f2f2f2;
  padding: 10px;
}
ul {
  list-style-type: none;
  display: flex;
  justify-content: start;
  gap: 12px;
}
</style>
