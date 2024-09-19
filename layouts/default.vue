<script setup></script>
<template>
  <div>
    <header>
      <nav>
        <ul>
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/images">Images</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/africa">Africa</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/america">America</NuxtLink>
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
