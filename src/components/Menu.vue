<script setup>

  const menuItems = [
    { name: 'Home', link: '#' },
    { name: 'About', link: '#' },
    { name: 'Contact', link: '#' }
  ]

</script>

<template>
  <ul>
    <li v-for="menuItem in menuItems">
      <a href="">{{ menuItem.name }}</a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
  ul {
    margin-top: 30px;
    display: flex;
    justify-content: space-around;
    list-style: none;
    padding: 0;
    li {
      a {
        background-color: #ccc;
        padding: 10px 20px;
        border-radius: 5px;
        text-decoration: none;
        color: #000;
        &:hover {
          background-color: violet;
        }
      }
    }
  }

</style>