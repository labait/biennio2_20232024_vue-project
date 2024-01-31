<script setup>
    const works= [
        {name: "work1", image: "https://source.unsplash.com/random/?green&random=1"},
        {name: "work2", image: "https://source.unsplash.com/random/?green&random=2"},
        {name: "work3", image: "https://source.unsplash.com/random/?green&random=3"},
    ]

    const questions= [
        {
            "question": "superpowers?",
            "options": [
                {
                    value: "fly", points: 1,
                    value: "strenght", points: 2,
                }
            ]
        }
    ]
</script>

<template>
    <h1>Works</h1>
    list of works
    <div class="container">
        <div class="row">
            <div class="col-12 col-md-4" v-for="work in works">
                <div class="title">{{ work.title }}</div>
                <img :src="work.image" alt="" class="img-fluid">
            </div>
        </div>
    </div>
</template>


