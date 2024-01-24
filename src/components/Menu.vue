<script setup>

  let period = "morning";
  const hours = new Date().getHours();
  if(hours > 10 ) period = "afternoon";
  if(hours > 20 ) period = "evening";
  const menuItems = [
    { name: 'Home', link: '#' },
    { name: 'About', link: '#' },
    { name: 'Contact', link: '#' },
    { name: 'logout', link: '#' },
  ]

</script>

<template>
  <div v-if="period == 'morning'">
    <h1>Buongiorno!</h1>
  </div>
  <div v-if="period == 'afternoon'">
    <h1>Buon pomeriggio!</h1>
  </div>
  <div v-if="period == 'evening'">
    <h1>Buonasera!</h1>
  </div>
  <!-- --><ul>
    <li v-for="menuItem in menuItems">
      <a href="">{{ menuItem.id }} {{ menuItem.name }}</a>
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