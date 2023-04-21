<template>
    <div>
        <h1 class="title">Welcome to {{name}}</h1>
        <p>{{desc}}</p>
        <button>See more</button>
    </div>
</template>

<script>
export default {
    name: "Profile component",
    props: [name, desc],
    data: () => ({

    }),
    methods: {
        
    },
}
</script>