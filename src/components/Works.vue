<script setup>
    import works from '../assets/works.js';
    import List from './List.vue';
    import Articles from './Articles.vue';

    const tags =  [...new Set(works.map(w => w.tags).flat())] //.sort()
    console.log(tags);
</script>

<template>
    <Articles />
    <h1>Seasons</h1>
    <div class="tag" v-for="tag in tags">
        <List :title="tag" :items="works.filter(w => w.tags.includes(tag))" />
    </div>
</template>


<style>

h1{  
  font-size: 5rem;
  font-weight: 700;
  text-align: center;
  margin-top: 1rem;
}

h2{  
  font-size: 2rem;
  font-weight: 500;
  margin-top: 2rem;
}

.title{ 
  font-size: 1rem;
  font-weight: 300;
  font-style: italic;
}

</style>