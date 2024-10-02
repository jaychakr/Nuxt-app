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
            <NuxtLink to="/accordion">Accordion</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/inputbox">Input Box</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/africa">Africa</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/america">Americas</NuxtLink>
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
  justify-content: center;
  gap: 12px;
}
@media (max-width: 600px) {
  nav {
    font-size: 12px;
  }
}
</style>
